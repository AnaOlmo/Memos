---


---

<h1 id="exemple-projet">Exemple projet:</h1>
<p>1-Créer un répertoire ​Hello_Again, avec un fichier ​HelloWorld.java​ qui contient:</p>
<pre><code>public class HelloWorld {
 public static void main(String[] args) { 
 System.out.println("Texte!"); 
  }
    }
</code></pre>
<p>Ce fichier est la définition d’une classe ​HelloWorld​, qui a une méthode statique (attachée  à la classe et non aux instances de cette classe) ​main​ (nous passons sur les arguments)  et qui utilise la méthode statique println de la classe ​System.out</p>
<p>Pour exécuter ce programme, il faut d’abord le compiler. Ouvrez un shell (cmd, bash, …) et  positionnez-vous dans le répertoire du fichier. Compilez et exécutez le programme comme  ceci :</p>
<pre><code>ls
javac HelloWorld.java
ls
java HelloWorld
</code></pre>
<p>La commande ​javac​ (Java Compiler) produit le fichier compilé ​HelloWord.class​. La  commande ​java HelloWorld​ exécute ces étapes :  - cherche la classe HelloWorld dans l’environnement (par défaut dans le répertoire  courant =&gt; définie dans ​HelloWord.class</p>
<ul>
<li>charge cette classe</li>
<li>cherche la méthode par défaut, ​main​ et l’exécute</li>
</ul>
<p>2- Créez l’arborescence de répertoires ​Hello_1/src/main/java/hello​. En utilisant Bash,  vous pouvez le faire avec la seule commande</p>
<h5 id="mkdir--p-hello_1srcmainjavahello">mkdir -p Hello_1/src/main/java/hello</h5>
<p>Créez dans le répertoire ​hello​ les deux fichiers ​Greeter.java ​et ​HelloWorld.java​ qui  contiennent respectivement :</p>
<pre><code>package hello; 
public class Greeter { 
public String sayHello() {
return "Hello world!"  ; 
 } 
  } 



package hello;
public class HelloWorld {
public static void main(String[] args) { 
Greeter greeter = new Greeter(); 
System.out.println(greeter.sayHello());
} 
} 
</code></pre>
<p>Le programme utilise maintenant deux classes et peut être compilé et exécuté comme suit  :</p>
<h5 id="ls">ls</h5>
<h5 id="javac-.java">javac *.java</h5>
<h5 id="ls-1">ls</h5>
<h5 id="java-hellohelloworld">java hello/HelloWorld</h5>
<h5 id="cd-..">cd …</h5>
<h5 id="ls-2">ls</h5>
<h5 id="java-hello.helloworld">java hello.HelloWorld</h5>
<h3 id="maven">MAVEN:</h3>
<p>permettent en général de  gérer des dépendances (modules externes) et le cycle de compilation<br>
Installez Maven en suivant les instructions du site <a href="http://maven.apache.org/">http://maven.apache.org/</a></p>
<p>L’utilisation de Maven repose sur un Project Object  Model (POM), ici un seul fichier ​pom.xml​, à côté sur répertoire ​src​ :</p>
&lt;?xml version="1.0" encoding="UTF-8"?&gt;     4.0.0 
<p>fr.campus-numerique-in-the-alps   hello   1     &lt;maven.compiler.source&gt;1.8&lt;/maven.compiler.source&gt;  &lt;maven.compiler.target&gt;1.8&lt;/maven.compiler.target&gt;  &lt;project.build.sourceEncoding&gt;UTF-8&lt;/project.build.sourceEncoding&gt;     </p>
<p>nous pouvons maintenant utiliser la commande ​mvn​ pour compiler les différents  fichiers .​java​ qui pourraient être répartis dans différents répertoires</p>
<h5 id="mvn-compile">mvn compile</h5>
<h5 id="ls--r--targetclasses">ls -R  target/classes</h5>
<h5 id="java--cp-targetclasses-hello.helloworld">java -cp target/classes hello.HelloWorld</h5>
<p>mvn compile​ déclenche la compilation du projet ​hello​, en version 1. Deux classes sont  trouvées et compilées, les fichiers .​class​ allant dans le répertoire ​target/classes​. Il faut  alors indiquer à Java le (ou les) chemin pour trouver les classes pour l’exécution. On utilise  ici l’option ​-cp​ (classpath) pour indiquer de chercher dans le répertoire ​target/classes​.</p>
<p>Maven ici “installe” le projet en créant le jarfile. Ce jarfile peut être passé comme un  répertoire pour indiquer un endroit où trouver des classes, via l’option ​-cp​ (le “classpath”).</p>
<h5 id="mvn-install">mvn install</h5>
<h5 id="java--cp-targethello-1.jar--hello.helloworld">java -cp target/hello-1.jar  hello.HelloWorld</h5>
<p>changer a nouveau file POM.xml  ( attention aux espaces!)<br>
utiliser un plugin Maven : “Shade”. Modifiez le fichier de projet :<br>
voir fichier POM details dans C:\wamp64\www\Java\Hello_Again</p>
<h5 id="java--jar-targethello-1.jar">java -jar target/hello-1.jar</h5>
<h2 id="une-interface-​bonjour​-avec-une-méthode-sayhello-qui-renvoie-un-chaîne-de--caractères-">une interface ​Bonjour​ avec une méthode sayHello qui renvoie un chaîne de  caractères ;</h2>
<pre><code>package  hello; (fichier source)
public  interface  Bonjour{
public  String  sayHello();
}
</code></pre>
<h2 id="une-classe-abstraite-​animal​-qui-implémente-l’interface">une classe abstraite ​Animal​, qui implémente l’interface</h2>
<pre><code>package  hello;
public  abstract  class  Animal  implements  Bonjour {
public  abstract  String  sayHello ();
}
</code></pre>
<h2 id="deux-classes-qui-étendent-​animal​-​human​-et-​dog​.">deux classes qui étendent ​Animal​, ​Human​ et ​Dog​.</h2>
<pre><code>package  hello;
public  class  Human  extends  Animal {
public  String  sayHello (){
return  "hello";
}
}
</code></pre>
<p>Créez une instance pour chacune des classes concrètes</p>
<pre><code>package  hello;
public  class  HelloWorld {
public  static  void  main(String\[\] args) {
Animal  maincoon  =  new  Cat();
Animal  charles  =  new  Human();
System.out.println(" tutut: "  +  maincoon.sayHello());
System.out.println(" toto: "  +  charles.sayHello());
}
}
</code></pre>
<p>une fois fait, utiliser ligne commande:<br>
mvn install<br>
java -cp target/hello-1.jar hello.HelloWorld</p>

