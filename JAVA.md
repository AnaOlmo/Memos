---


---

<h1 id="exos">Exos</h1>
<h2 id="data-types"><em>data types</em></h2>
<h3 id="string">String</h3>
<p>public class YourName {<br>
public static void main(String[] args) {</p>
<pre><code>	System.out.println("Ana-Maria");

}
</code></pre>
<p>}</p>
<h3 id="int">Int</h3>
<p>public class DataTypes {<br>
public static void main(String[] args) {</p>
<pre><code>	System.out.println(450);

}
</code></pre>
<p>}</p>
<h3 id="boolean">Boolean</h3>
<p>public class DataTypesB {<br>
public static void main(String[] args) {</p>
<pre><code>	System.out.println(true);

}
</code></pre>
<p>}</p>
<h3 id="char">Char</h3>
<p>public class DataTypesC {<br>
public static void main(String[] args) {</p>
<pre><code>	System.out.println('Z');

}
</code></pre>
<p>}</p>
<h2 id="variables">Variables</h2>
<p>the ability to store values using  <em>variables</em>.</p>
<ol>
<li>
<p>A  <em>variable</em>  stores a value.</p>
</li>
<li>
<p>In Java, all variables must have a specified data type</p>
</li>
</ol>
<p>public class Variables {<br>
public static void main(String[] args) {</p>
<pre><code>	int myNumber = 42;
	boolean isFun = true; 
	char movieRating ='A'; 

}
</code></pre>
<p>}</p>
<h2 id="whitespace">Whitespace</h2>
<p>is often used to make code visually presentable.</p>
<h5 id="before">Before:</h5>
<p>public class WhiteSpace {<br>
public static void main(String[] args) {</p>
<pre><code>	boolean isFormatted = false;System.out.println(isFormatted);

}
</code></pre>
<p>}</p>
<h5 id="after">After:</h5>
<p>public class WhiteSpace {<br>
public static void main(String[] args) {</p>
<pre><code>	boolean isFormatted = false;
	System.out.println(isFormatted);
}
</code></pre>
<p>}</p>
<h2 id="comments">Comments</h2>
<p>// I’m a single line comment!<br>
Multiple lines comment : /*  Hello, Java! */</p>
<h2 id="math-----and-">Math: +, -, *, and /</h2>
<p>public class Arithmetic {<br>
public static void main(String[] args) {</p>
<pre><code>	int myNumber = 123 * 456;
	System.out.println(myNumber);

}
</code></pre>
<p>}</p>
<h2 id="math-">Math: %</h2>
<ol>
<li>e  <em>modulo</em>  operator - represented in Java by the  <code>%</code>  symbol - returns the remainder of dividing two numbers.</li>
</ol>
<p>For example,  <code>15 % 6</code>  will return the value of  <code>3</code>, because that is the remainder left over after dividing 15 by 6.</p>
<p>public class Modulo {<br>
public static void main(String[] args) {</p>
<pre><code>	int myRemainder = 16 % 7;
	System.out.println(myRemainder);

}
</code></pre>
<p>}</p>
<h2 id="relational-operators">Relational Operators</h2>
<p>Here are a few relational operators:</p>
<ol>
<li><code>&lt;</code>  : less than.</li>
<li><code>&lt;=</code>: less than or equal to.</li>
<li><code>&gt;</code>: greater than.</li>
<li><code>&gt;=</code>: greater than or equal to.</li>
</ol>
<p>public class RelationalOperators {<br>
public static void main(String[] args) {</p>
<pre><code>	System.out.println(25 &gt; 12);

}
</code></pre>
<p>}</p>
<h2 id="equality-operators">Equality Operators</h2>
<p>The equality operators are:</p>
<ol>
<li>
<p><code>==</code>: equal to.</p>
</li>
<li>
<p><code>!=</code>: not equal to.<br>
public class EqualityOperators {<br>
public static void main(String[] args) {</p>
<pre><code>System.out.println(true == false);
</code></pre>
<p>}<br>
}</p>
</li>
</ol>
<h2 id="conditionnal">Conditionnal</h2>
<p>public class Conditionals {<br>
public static void main(String[] args) {</p>
<pre><code>	if (1 &lt; 4 &amp;&amp; 0 &gt; 5) {

		System.out.println("You ordered a cup of hot, mint tea.");

	} else if (21 &lt;= 19 || 17 &gt;= 28) {
		
		System.out.println("You ordered freshly squeezed orange juice!");

	} else if ( !(true == true) ) {

		System.out.println("You ordered hot cocoa!");

	} else {

		System.out.println("You ordered a cup of Java!");

	}

	char answerChoice = 'C';

	switch (answerChoice) {

		case 'A': System.out.println("You answered: " + answerChoice + ". Please try again.");
							break; 

		case 'B': System.out.println("You answered: " + answerChoice + ". Please try again.");
							break;

		case 'C': System.out.println("You answered: " + answerChoice + ". That is correct!");
							break;

		case 'D': System.out.println("You answered: " + answerChoice + ". Please try again.");
							break;

		default:
			System.out.println("Please select a valid answer choice.");

	}


}
</code></pre>
<p>}</p>
<p>The  <em>precedence</em>  of each Boolean operator is as follows:</p>
<ol>
<li><code>!</code>  is evaluated first</li>
<li><code>&amp;&amp;</code>  is evaluated second</li>
<li><code>||</code>  is evaluated third<br>
&amp;&amp; : and<br>
|| : or<br>
! : opposite</li>
</ol>
<p>public class Precedence {<br>
public static void main(String[] args) {</p>
<pre><code>	boolean riddle = (! (1 &lt; 8) || (5 &gt; 2 &amp;&amp; 3 &lt; 5));
	System.out.println(riddle);

}
</code></pre>
<p>}</p>
<h2 id="if-elseif-else-statement">If-ElseIf-Else Statement</h2>
<p>public class IfElseIf {<br>
public static void main(String[] args) {</p>
<pre><code>	int round=11;

	if (round &gt; 12) {

		System.out.println("The match is over!");

	} else if (round &gt; 0) {

		System.out.println("The match is underway!");

	}	else {

		System.out.println("The boxing match hasn't started yet.");

	}	
}
</code></pre>
<p>}</p>
<h3 id="ternary-conditional-statement"><em>ternary conditional</em> statement</h3>
<p>public class Ternary {<br>
public static void main(String[] args) {</p>
<pre><code>	int fuelLevel = 3;

	char canDrive =(fuelLevel &gt;0) ? 'Y':'N';
	System.out.println(canDrive);

}
</code></pre>
<p>}</p>

