# cs6250-project-4--spanning-tree-solved
**TO GET THIS SOLUTION VISIT:** [CS6250 Project 4- Spanning Tree Solved](https://mantutor.com/product/cs6250-spanning-tree-solved-3/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;97962&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS6250 Project 4- Spanning Tree Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
PROJECT GOAL

In the lectures, you learned about Spanning Trees (see Canvas-&gt;Modules-&gt;Lesson 1-&gt; “Looping Problem in Bridges and the Spanning Tree Algorithm), which can be used to prevent forwarding loops on a layer 2 network (see the Wikipedia entry on Spanning Trees. In this project, you will develop a simplified distributed version of the Spanning Tree Protocol that can be run on an arbitrary layer 2 topology. With this project, we will be simulating the communications between switches until they converge on a single solution, and then output the final spanning tree to a file.

Part 1: Setup

Download the project from Canvas to the course VM and unzip. Alternatively, you can do this project on your host system if it has Python 3.7 or newer installed… just be sure that it runs properly in the VM, as this is where we run the autograder.

Ensure the files have the correct permissions. (See the Simulating Networks project if you need a refresher on basic Linux commands.) This project MUST be coded in Python 3.7 or newer – the VM has Python 3.8, otherwise make sure your host’s Python version is updated to 3.7 or newer.

Part 2: Files Layout

There are many files in the SpanningTree directory, but you only need to (and should only) modify Switch.py, which represents a layer 2 switch that implements our simple Spanning Tree Protocol. You will implement the functionality of the Spanning Tree Protocol to generate a Spanning Tree for each Switch. (Details follow in the “2. Project Outline – TODOs”.)

The other files in the project skeleton are described below. Do not modify these files, all of your coding will be in Switch.py. However please study these files to understand the project better and to make decisions about your code in Switch.py.

• Topology.py – Represents a network topology of layer 2 switches. This class reads in the specified topology and arranges it into a data structure that your switch code can access.

• StpSwitch.py – A base class of the derived class you will code in Switch.py. The base class StpSwitch.py abstracts certain implementation details to simplify your tasks.

• Message.py – This class represents a simple message format you will use to communicate between switches, similar to what was described in the course lectures.

Specifically, you will create and send messages in Switch.py by declaring a message as msg = Message(claimedRoot, distanceToRoot, originID, destinationID, pathThrough)

• run_spanning_tree.py – A simple “main” file that loads a topology file (see XXXTopo.py below), uses that data to create a Topology object containing Switches, and starts the simulation.

• XXXTopo.py, etc. – These are topology files that you will pass as input to the run_spanning_tree.py file.

• sample_output.txt – Example of a valid output file for Sample.py as described in the comments in Switch.py.

Part 3: TODOs

This is an outline of the code to implement in Switch.py with suggestions for implementation. Your implementation must adhere to the “spirit of the project” and satisfy the labeled TODO sections in the project code per the pre-existing comments.

A. Decide on the data structure that you will use to keep track of the spanning tree.

1. The collection of active links across all switches is the resultant spanning tree.

3. This is a distributed algorithm. The switch can only communicate with its neighbors.

It does not have an overall view of the spanning tree, or of the topology as a whole.

4. An example data structure would include, at a minimum:

a. a variable to store the switch ID that this switch currently sees as the root,

b. a variable to store the distance to the switch’s root,

c. a list or other datatype that stores the “active links” (i.e., the links to neighbors that should be drawn in the spanning tree).

d. a variable to keep track of which neighbor it goes through to get to the root. (A switch should only go through one neighbor, if any, to get to the root.)

6. It is important to create a data structure in the correct place in Python (and most object- oriented programming languages). If you create it inside a method, every time the method is called it will be created as new. You should create a class object in the class constructor so that the data stored in the object exists for the life of the class instance that is created by Topology.py. For example self.mylist = [ ] in the constructor should create an empty list data structure and act as instance variable. But if mylist were instantiated in, say, process_messages, then it will be created every time the method is called. This could be useful in how you track which links are active to certain neighbors for any given switch.

B. Implement sending initial messages to neighbors of the switch.

1. Your implementation of send_initial_messages() in Switch.py will be called in Topology.py for each switch in the topology before any other messages are processed and/or sent.

2. See code comments in Message.py, Topology.py, and StpSwitch.py for details on message format, message creation, and how to send messages between switches.

a. pathThrough is a Boolean, not an int.

b. In a message, pathThrough is TRUE if the message-sending switch goes through the message-receiving switch in order to reach claimedRoot. pathThrough is FALSE if the message-sending switch does not go through the message-receiving switch in order to reach claimedRoot.

3. Initially, each switch thinks it is the root of the spanning tree.

C. Implement processing a message from an immediate neighbor.

1. For each message a switch receives, the switch will need to:

a. Determine whether an update to the switch’s root information is necessary and update accordingly.

I. The switch should update the root stored in its data structure if it receives a message with a lower claimedRoot.

II. The switch should update the distance stored in its data structure if

a) the switch updates the root, or b) there is a shorter path to the same root.

b. Determine whether an update to the switch’s active links data structure is necessary and update accordingly. The switch should update the activeLinks stored in the data structure if:

I. The switch finds a new path to the root (through a different neighbor). In this case, the switch should add the new link to activeLinks and (potentially) remove the old link from activeLinks

II. The switch receives a message with pathThrough = TRUE but does not have that originID in its activeLinks list. In this case, the switch should add originID to its activeLinks list.

c. Determine whether the switch should send new messages to its neighbors and send messages accordingly.

I. This is an important design decision. There are many correct algorithms that send messages at different times. The distributed algorithm has converged to the Spanning Tree when no more messages are sent.

II. The message FIFO queue is maintained in Topology.py. The switch implementation does not interact with the FIFO queue directly, but instead uses send_msg to send messages, and receives a message as an argument in process_message. iii. When sending messages, pathThrough should only be TRUE if the destinationID switch is the neighbor that the originID switch goes through to get to the claimedRoot. Otherwise, pathThrough should be FALSE.

D. Write a logging function that is specific to your particular data structure.

1. The switch should only output the links that it thinks are in spanning tree.

2. Follow the format. Unsorted/non-standard formatting can result in autograder penalties. Examples of correct solutions with correct format have been provided to you.

3. Sorted: Not sorted:

1 – 2, 1 – 3 1 – 3, 1 – 2

2 – 1, 2 – 4 2 – 4, 2 – 1

3 – 1 3 – 1

4 – 2 4 – 2

Part 4: Testing and Debugging

To run your code on a specific topology (SimpleLoopTopo.py in this case) and output the results to a text file (out.txt in this case), execute the following command:

python run_spanning_tree.py SimpleLoopTopo out.txt

NOTE: “SimpleLoopTopo” is not a typo in the example command – don’t include the .py extension.

We have included several topologies with correct solutions (and format) for you to test your code against. You can (and are encouraged to) create more topologies with output files and share them on Ed Discussion.

You will only be submitting Switch.py – your implementation must be confined to modifications to that file. We recommend testing your submission against a clean copy of the rest of the project files prior to submission.

We encourage adding print statements to facilitate debugging during the development process, if they are removed or commented out prior to submission.

Part 5: Assumptions and Clarifications

A. All switch IDs are positive integers, and distinct.

1. These integers do not have to be consecutive.

2. They will not always start at 1.

3. There is no maximum value beyond language (Python) limitations (which your code does not need to check for).

B. Tie breakers: If there are two paths of equal distance to the same root, the switch should choose the path through the neighbor with the lowest switch ID.

1. Example: switch 5 has two paths to root switch 1, through switch 3 and switch 2. Each path is 2 hops in length. Switch 5 should select switch 2 as the path to the root and disable forwarding on the link to switch 3.

C. There is a single distinct solution spanning tree for each topology. This is guaranteed by the first two assumptions.

D. All switches in the network will be connected to at least one other switch, and all switches are able to reach every other switch. It will always be possible to form a tree that spans the entire topology.

E. There will be only 1 link between each pair of directly connected switches. You do not need to consider how STP should behave with redundant links.

F. The topology given at the start will be the final topology. The topology will not change while your code is running (i.e., adding a switch, severing a connection, etc.)

H. The solution implemented in Switch.py should terminate without intervention. When there are no more messages in the queue to process, the simulation will log output and self-terminate.

What to Turn In

• Switch.py

Before submission:

a. Make sure your logging format is correct. Invalid format will result in autograder penalties.

b. Remove any print statements from your code before turning it in. Print statements left in the simulation, especially for inefficient implementations, have drastic effects on runtime. Your submission should take less than 10 seconds to process a topology used in grading. If print statements in your code adversely affect the grading process, your work will not receive full credit.

c. Make sure your Switch.py works in the virtual machine, where we will run the autograder. When done, submit to Canvas. Then, in the VM, log into Canvas and download your submission and test it out to make sure it works there. You’ll need to download the project files as well and drop in your Switch.py.

After submission:

What you can and cannot share

Rubric

15

pts Correct

Submission For turning in all the correct files with the correct names, and significant effort has been made in each file towards completing the project.

60

pts Provided

Topologies For correct Spanning Tree results (log files) on the provided topologies.

75

pts Unannounced

GRADING NOTE: Partial credit is not available for individual topology spanning tree output files. The output spanning tree must be fully correct to receive credit for that input topology – a single link’s discrepancy will result in a zero for that topology. Additionally, we will be using many topologies to test your project, including but not limited to the topologies we provide, and checking for corner cases not exhibited in the sample topologies provided.

The goal of this project is to implement a simplified version of a network protocol using a distributed algorithm. This means that your algorithm should be implemented at the network switch level. Each switch only knows its internal state, and the information passed to it via messages from its direct neighbors – the algorithm must be based on these messages.
