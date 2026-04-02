<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bash Scripting</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="bash-script">Bash Script</h1>
<p>Bash scripting is about writing scripts (programs) for the Unix/Linux shell to automate tasks. It’s widely used for <strong>system admin, DevOps, and everyday command-line workflows</strong>.</p>
<ul>
<li>
<p>Bash stands for <strong>Bourne Again Shell</strong></p>
</li>
<li>
<p>It is a <strong>command-line interpreter</strong></p>
</li>
<li>
<p>Default shell in most Linux systems</p>
</li>
<li>
<p>Used to interact with the OS</p>
</li>
<li>
<p>Writing a sequence of commands in a file</p>
</li>
<li>
<p>File usually has <strong><code>.sh</code></strong> extension</p>
</li>
<li>
<p>Automates repetitive tasks</p>
</li>
<li>
<p>Executes commands line by line</p>
</li>
</ul>
<h3 id="bash">Bash</h3>
<ul>
<li>
<p>A <strong>shell</strong> is a program that lets you interact with the operating system</p>
</li>
<li>
<p>Bash is powerful because it combines <strong>command execution +<br>
programming + automation</strong> in one place.</p>
</li>
<li>
<p>A <strong>scripting language</strong> you can write logic (loops, conditions, variables)</p>
</li>
</ul>
<h3 id="features-of-bash">features of bash</h3>
<ul>
<li>Command execution</li>
<li>Scripting capability</li>
<li>Pipes and redirection</li>
</ul>
<h3 id="bash-script-1">Bash Script</h3>
<p>A <strong>bash script</strong> is a text file that contains a series of commands written for the <strong>Bash shell</strong> (a command-line interpreter commonly used on Linux and macOS). Instead of typing commands one by one into the terminal, you can put them into a script and run them all at once.</p>
<p><strong>A file end with <code>.sh</code></strong></p>
<h2 id="key-components-of-bash-scripts">Key Components of Bash Scripts</h2>
<p>The <strong>key components of a Bash script</strong> are the basic building blocks that make the script work.</p>
<h3 id="shebang-interpreter-line">1) Shebang (Interpreter line)</h3>
<p>The <strong>shebang</strong> (also called the <em>interpreter directive</em>) is the very first line in a script that tells the operating system <strong>which interpreter should execute the file</strong>.</p>
<pre><code>#!/bin/bash
</code></pre>
<h3 id="comments">2) Comments</h3>
<p>Comments are used to explain your code, they are ignore by the shell during execution.</p>
<p><strong>Single line comments</strong></p>
<pre><code>#explain a code
</code></pre>
<p><strong>Multiline comment</strong></p>
<p>end with same first and last name same</p>
<pre><code>&lt;&lt; comment
explain code
comment
</code></pre>
<h3 id="variables">3) Variables</h3>
<p>Variables in shell scripting(bash) are used to store data that you can reuse throught your script.<br>
<strong>They are simply but very powerful</strong></p>
<p>Variables are <strong>Mutable</strong> (their values can be changed).</p>
<ul>
<li>Variables are case sensitive</li>
<li>Avoid using special character or reserved words</li>
<li>There are no data types, all variables in Bash are strings</li>
<li>use lowercase for variables &amp; upper case for constant</li>
<li>They valid only in a shell</li>
</ul>
<p><strong>Declaring variable</strong></p>
<pre><code>name=More
</code></pre>
<p><strong>Reading variable value</strong></p>
<pre><code>echo "name = $name"
		or
echo $name
</code></pre>
<p><strong>i) Environment Variables</strong> :-</p>
<p>Environment variables are a core concept in Bash and Unix-like systems. They are <strong>named values stored in the shell that affect how processes behave</strong> and can be shared with child processes.</p>
<p>ex:</p>
<pre><code>echo $HOME
</code></pre>
<p>output:</p>
<pre><code>/home/user
</code></pre>
<p><strong>ii) Reading Variable</strong><br>
It is taking input from the user and storing it in a variable. This is done using the <code>read</code> command.<br>
ex :</p>
<pre><code>read variable_name
</code></pre>
<p>Options</p>
<ul>
<li>-p : prompt a message</li>
<li>-d : set delimiter</li>
<li>-s : hide the input values</li>
</ul>
<p><strong>iii) Deleting Variables</strong><br>
Deleting variables in Bash is straightforward</p>
<pre><code>unset
</code></pre>
<p><strong>basic deletion</strong></p>
<pre><code>unset variable_name
</code></pre>
<p><strong>Environment variables</strong></p>
<pre><code>export NAME="More"
unset NAME
</code></pre>
<h3 id="a-simple-addition-program">A Simple addition program</h3>
<pre><code># Shebang line
#!/bin/bash  
x=10
y=20
result="$x + $y"
add_result=$(( x + y ))
echo "addition = $add_result"
</code></pre>
<h2 id="arrays">Arrays</h2>
<p><strong>Arrays is a store a multiple values in a single variables.</strong><br>
Array is a collection of similar or dissimilar types, and it is very useful when <strong>working with lists</strong> of items like files, names, or numbers.</p>
<p><strong>Declare an array</strong></p>
<pre><code>arr=(apple mango guava)
</code></pre>
<p><strong>Accessing an elements</strong></p>
<p>Read the <strong>first value</strong></p>
<pre><code>echo ${arr[0]}  # 0 is a index number
</code></pre>
<p>Read the <strong>last element</strong></p>
<pre><code>echo ${arr[2]}  #(2) you known a index value
echo ${arr[-1]}
</code></pre>
<p>Read the <strong>all element</strong></p>
<pre><code>echo ${arr[0]}
</code></pre>
<p>Find the <strong>length of array</strong></p>
<pre><code>echo ${#arr[@]}
</code></pre>
<p><strong>Add</strong> a new element</p>
<pre><code>arr=$( "${fruits[@]}" "pineapple")
echo ${arr[@]}
</code></pre>
<p><strong>Remove</strong> a element</p>
<pre><code>unset arr[2]
echo ${arr[@]}
</code></pre>
</div>
</body>

</html>
