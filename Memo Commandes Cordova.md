---


---

<p>MEMO CORDOVA</p>
<h2 id="les-commandes-cordova">Les commandes Cordova</h2>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>cordova create <path></path></td>
<td>$ npm install -g cordova</td>
</tr>
<tr>
<td>cordova create NomApplication</td>
<td>Créer un nouveau projet (création de l’intégralité du dossier)</td>
</tr>
<tr>
<td>cordova platform add </td>
<td>$ cd MyApp - $ cordova platform add browser /add android</td>
</tr>
<tr>
<td>cordova platform</td>
<td>Liste plateformes</td>
</tr>
<tr>
<td>Si erreur “command not found” avec CD MyApp</td>
<td>1.  Click on the <strong>Start</strong> menu in the lower-left corner of the desktop 2.  In the search bar, search for <strong>Environment Variables</strong> and select <strong>Edit the system Environment Variables</strong> from the options that appear 3.  In the window that appears, click the <strong>Environment Variables</strong> button ##### To create a new environment variable:[] (<a href="http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#to-create-a-new-environment-variable">http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#to-create-a-new-environment-variable</a>) 1.  Click <strong>New…</strong> and enter the variable name and value ##### To set your <strong>PATH</strong>:<a href="http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#to-set-your-path"></a> 1.  Select the <strong>PATH</strong> variable and press <strong>Edit</strong>. 2.  Add entries for the relevant locations to the <strong>PATH</strong> (c:/users/anaolmo/roaming/npm), move up.</td>
</tr>
<tr>
<td>cordova run </td>
<td>$ cordova run browser et $ cordova run android</td>
</tr>
<tr>
<td>cordova plugin add </td>
<td>exemple $ cordova plugin add cordova-plugin-camera</td>
</tr>
</tbody>
</table><h2 id="structure-d’un-projet-cordova">Structure d’un projet Cordova</h2>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Contenu du répertoire “platforms”</td>
<td>dossiers Android et Browser et sous dossiers Gradle / JSON- différentes plateformes ajoutées au projet</td>
</tr>
<tr>
<td>Contenu du répertoire “plugins”</td>
<td>Fichiers JSON: Android-Fetch-Browser et Cordova plugin whitelist - différents plugins installés pour le projet</td>
</tr>
<tr>
<td>Contenu du répertoire “www”</td>
<td>CSS-Images-JS-Index.html - fichiers de développement</td>
</tr>
<tr>
<td>Contenu du fichier “package.json”</td>
<td>liste les dépendances, des fonctionnalités du projet, spécifie la version du package.</td>
</tr>
<tr>
<td>Contenu du fichier “config.xml”</td>
<td>Fichier de configuration de Cordova: XML est un fichier texte utilisant des balises pour l’échange de données automatisés entre systèmes.</td>
</tr>
<tr>
<td>Contenu du fichier “www/index.html”</td>
<td>contient la vue du browser- Page d’accueil du projet</td>
</tr>
</tbody>
</table><h2 id="installer-android-studio">Installer Android Studio</h2>
<ul>
<li>Télécharger Android Studio : (<a href="https://developer.android.com/studio/index.html">https://developer.android.com/studio/index.html</a>)</li>
<li>Aide à l’installation :<br>
(<a href="https://developer.android.com/studio/install.html">https://developer.android.com/studio/install.html</a>)</li>
</ul>
<h2 id="installer-node.js">Installer Node.js</h2>
<ul>
<li>Télécharger Node.js : (<a href="https://nodejs.org/fr/">https://nodejs.org/fr/</a>)</li>
</ul>
<h2 id="installer-cordova">Installer Cordova</h2>
<p>Infos installation : (<a href="http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html">http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html</a>)</p>
<h3 id="installer-jdk-java-development-kit"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#installer-jdk-java-development-kit"></a>Installer JDK (Java Development Kit)</h3>
<ul>
<li>Télécharger la V161 : (<a href="http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html">http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html</a>)</li>
</ul>
<h3 id="installer-cordova-1"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#installer-cordova-1"></a>Installer Cordova</h3>
<ul>
<li>Ouvrir un Bash, vérifier la présence de Node.js</li>
</ul>
<pre><code>node -v  

</code></pre>
<ul>
<li>Installer Cordova :</li>
</ul>
<pre><code>npm install -g cordova  
</code></pre>
<ul>
<li>Changer le PATH</li>
<li>Windows + Pause</li>
<li>Paramètres système avancés</li>
<li>Variables d’environnement</li>
<li>PATH</li>
<li>Récupérer le chemin de NPM : C:\Users\ana-maria.olmo\AppData\Roaming\npm</li>
<li>Nouveau : copier le chemin</li>
<li>Déplacer vers le haut dans la liste</li>
</ul>
<h1 id="projet-application"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#projet-application"></a>Projet Application</h1>
<p>Informations sur la création d’un projet : (<a href="http://cordova.apache.org/#getstarted">http://cordova.apache.org/#getstarted</a>)</p>
<h2 id="créer-un-projet">Créer un projet</h2>
<p>Ligne de commande permettant de créer le dossier complet pour l’App :</p>
<pre><code>cordova create NomApplication  

</code></pre>
<h2 id="ajouter-une-plateforme"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#ajouter-une-plateforme"></a>Ajouter une plateforme</h2>
<p>Pour connaître toutes les plateformes, se positionner dans le dossier puis :</p>
<pre><code>cordova platform  

</code></pre>
<p>Ajouter une plateforme web :</p>
<pre><code>cordova platform add browser  

</code></pre>
<h2 id="faire-tourner-l’application"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#faire-tourner-lapplication"></a>Faire tourner l’application</h2>
<p>Ligne de commande :</p>
<pre><code>cordova run NomPlateforme  

</code></pre>
<p>Le projet est en ligne sur : localhost:8000<br>
Le projet est compilé.</p>
<h2 id="emuler-android"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#emuler-android"></a>Emuler Android</h2>
<p>Pour que notre ordinateur puisse fonctionner comme un Android, il faut émuler un Android</p>
<ul>
<li>Redémarrer l’ordinateur et pendant le redémarrage appuyer 2 ou 3 fois sur “Echap”</li>
<li>Dans le menu qui s’ouvre aller dans BIOS SetUp en cliquant ou appuyer sur F10</li>
<li>Aller dans l’onglet “Advanced”</li>
<li>Choisir “Systems Options”</li>
<li>Cocher les cases “Virtualization”</li>
<li>Save (puis confirmer l’enregistrement)</li>
</ul>
<h2 id="faire-tourner-l’application-sur-la-plateforme-android"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#faire-tourner-lapplication-sur-la-plateforme-android"></a>Faire tourner l’application sur la plateforme Android</h2>
<h3 id="sélectionner-la-bonne-plateforme"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#s%C3%A9lectionner-la-bonne-plateforme"></a>Sélectionner la bonne plateforme</h3>
<p>Si la commande “cordova run android” donne une erreur et indique qu’il n’y a pas le “plateforme 26”, cela peut se régler dans Android Studio</p>
<ul>
<li>Ouvrir dans Android Studio : Configure / Settings / System Settings / Android SDK</li>
<li>Cocher la plateforme 26 (colonne “API Level”) et appliquer</li>
</ul>
<h3 id="tout-fonctionne-"><a href="https://github.com/SylvainThibault/Memos/blob/master/M%C3%A9mo%20Cordova%20Install.md#tout-fonctionne-"></a>Tout fonctionne ?</h3>
<p>Dans Android Studio, l’onglet “Tools” il doit y avoir “Android”</p>
<p>Paramétrer ensuite le téléphone souhaité pour la visualisation.</p>

