<p align="center"> 
  <img src="gif/pacman_game.gif" alt="Animated gif pacman game" height="282px" width="637">
</p>
<h1 align="center"> Pacman with AI</h1>
<h3 align="center"> Astadeus Team </h3>

<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> :book: Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#overview"> ➤ Overview</a></li>
    <li><a href="#project-files-description"> ➤ Project Files Description</a></li>
    <li><a href="#getting-started"> ➤ Getting Started</a></li>
    <li><a href="#scenario1"> ➤ Scenario 1: Depth First Search </a></li>
    <li><a href="#scenario2"> ➤ Scenario 2: Breadth First Search </a></li>
    <li><a href="#scenario3"> ➤ Scenario 3: Uniform Cost Search </a></li>
    <li><a href="#scenario4"> ➤ Scenario 4: A* search algorithm </a></li>
    <li><a href="#scenario5"> ➤ Scenario 5: Finding All Corners </a></li>
    <li><a href="#scenario7"> ➤ Scenario 6: Eating All Dots </a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- OVERVIEW -->
<h2 id="overview"> :cloud: Overview</h2>

<p align="justify"> 
  In this project, the Pacman agent will find paths through his maze world, both to reach a particular location and to collect food efficiently. I implemented general search algorithms such as depth-first, breadth-first, uniform cost, and A* search algorithms which are used to solve navigation problems in the Pacman world.
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- PROJECT FILES DESCRIPTION -->
<h2 id="project-files-description"> :floppy_disk: Project Files Description</h2>

<ul>
  <li><b>search.py</b> - Where all of the search algorithms reside.</li>
  <li><b>searchAgents.py</b> - Where all of the search-based agents reside.</li>
  <li><b>pacman.py</b> - The main file that runs Pacman games. This file also describes a Pacman GameState types.</li>
  <li><b>game.py</b> - The logic behind how the Pacman world works.</li>
  <li><b>util.py</b> - Useful data structures for implementing search algorithms.</li>
</ul>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- GETTING STARTED -->
<h2 id="getting-started"> :book: Getting Started</h2>

<p>You are able to start the game by typing the following commands in the command line:</p>
<pre><code>$ python pacman.py</code></pre>

<p>You can see the list of all options and their default values via:</p>
<pre><code>$ python pacman.py -h</code></pre>
<i>Note that all of the commands that appear in this project also appear in <code>commands.txt</code>, for easy copying and pasting.</i>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- SCENARIO1 -->
<h2 id="scenario1"> :small_orange_diamond: Scenario 1: Finding a Fixed Food Dot using Depth First Search</h2>

<p>I have implemented the depth-first search (DFS) algorithm in the depthFirstSearch function in <code>search.py</code>.</p>
<p>The Pacman will quickly find a solution via running the following commands:</p>

<pre><code>$ python pacman.py -l tinyMaze -p SearchAgent</code></pre>
<pre><code>$ python pacman.py -l mediumMaze -p SearchAgent</code></pre>
<pre><code>$ python pacman.py -l bigMaze -z .5 -p SearchAgent</code></pre>

<p align="center"> 
<img src="gif/DFS.gif" alt="Animated gif DFS Algorithm" height="282px" width="637px">
<!--height="382px" width="737px"-->
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- SCENARIO2 -->
<h2 id="scenario2"> :small_orange_diamond: Scenario 2: Finding a Fixed Food Dot using Breadth First Search</h2>

<p>I have implemented the breadth-first search (BFS) algorithm in the breadthFirstSearch function in <code>search.py</code>.</p>
<p>I wrote a graph search algorithm that avoids expanding any already visited states.</p>
<p>The Pacman will quickly find a solution via running the following commands:</p>

<pre><code>$ python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs</code></pre>
<pre><code>$ python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5</code></pre>

<p align="center"> 
<img src="gif/BFS.gif" alt="Animated gif BFS Algorithm" height="282px" width="637">
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- SCENARIO3 -->
<h2 id="scenario3"> :small_orange_diamond: Scenario 3: Finding the best path using Uniform Cost Search</h2>

<p>I have implemented the uniform-cost graph search (UCS) algorithm in the uniformCostSearch function in <code>search.py</code>.</p>
<p>While BFS will find a fewest-actions path to the goal, UCS will find paths that are “best” in other senses.</p>
<p>UCS agents differ only in the cost function they use.</p>
<p>The Pacman will quickly find a solution via running the following commands:</p>

<pre><code>$ python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs</code></pre>
<pre><code>$ python pacman.py -l mediumDottedMaze -p StayEastSearchAgent</code></pre>
<pre><code>$ python pacman.py -l mediumScaryMaze -p StayWestSearchAgent</code></pre>

<p align="center"> 
<img src="gif/UCS.gif" alt="Animated gif UCS Algorithm" height="282px" width="637">
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- SCENARIO4 -->
<h2 id="scenario4"> :small_orange_diamond: Scenario 4: Finding the best path using A* search algorithm</h2>

<p>I have implemented the A* graph search algorithm in the aStarSearch function in <code>search.py</code>.</p>
<p>I used Manhattan distance as the heuristic function.</p>
<p>A* finds the optimal solution slightly faster than Uniform Cost Search.</p>
<p>The Pacman will quickly find a solution via running the following command:</p>

<pre><code>$ python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic</code></pre>

<p align="center"> 
<img src="gif/A.gif" alt="Animated gif A* search Algorithm" height="420px" width="420px">
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- SCENARIO5 -->
<h2 id="scenario5"> :small_orange_diamond: Scenario 5: Finding All the Corners</h2>

<p>I have implemented a search algorithm in <code>searchAgents.py</code> that helps Pacman agent to find the shortest path through the maze that touches all four corners.</p>

<p>The Pacman will quickly find a solution via running the following commands:</p>

<pre><code>$ python pacman.py -l tinyCorners -p SearchAgent -a fn=bfs,prob=CornersProblem</code></pre>
<pre><code>$ python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem</code></pre>

<p align="center"> 
<img src="gif/All Corners.gif" alt="Animated gif Finding All of the Corners" height="40%" width="40%">
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- SCENARIO6 -->
<h2 id="scenario6"> :small_orange_diamond: Scenario 6: Eating All of The Dots</h2>

<p>I have implemented a heuristic function that helps Pacman agent to eat all the food in as few steps as possible.</p>
<p>The Pacman will quickly find a solution via running the following command:</p>

<pre><code>$ python pacman.py -l trickySearch -p AStarFoodSearchAgent</code></pre>

<p align="center"> 
<img src="gif/All Dots.gif" alt="Animated gif Eating All of The Dots" height="282px" width="637">
</p>

