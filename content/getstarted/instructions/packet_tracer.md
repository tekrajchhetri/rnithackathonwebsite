---
title: Packet Tracer
date: '2023-01-22'
type: book
weight: 20
math: true
---


## Introduction
<p style="text-align: justify;">
Packet Tracer, also referred to as Cisco Packet Tracer, is a network simulation software developed by Cisco Systems. It allows users to design, configure, and simulate network topologies, including various Cisco devices and protocols such as BGP. Packet Tracer is commonly used in computer networking education and training, as well as for network design and troubleshooting. 
</p> 
<p style="text-align: justify;">
	This overview of the packet tracer is in no way a comprehensive tutorial. Visit the official Cisco website for comprehensive and in-depth Packet Tracer information.
</p>

## Packet Tracer Environment

<p style="text-align: justify;">
	Packet Tracer provides a graphical user interface (GUI) that allows users to design, configure, and simulate network topologies. Figure 1 shows the GUI interface of the Packet Tracer. The interface includes a variety of tools and features that make it easy to design and test network configurations, including drag-and-drop functionality for adding devices, a visual representation of the network, and the ability to configure device settings and protocols. We will look into some of the important components that we can see in Figure 1.
</p>

{{< figure src="../packet_tracer_start_page.png" caption="Figure 1: Packet Tracer Interface" >}}
<p style="text-align: justify;">
Figure 2 highlights the network components that are present on the bottom left corner of the Packet Tracer interface (see Figure 1). This is something that you will be using most often, and it contains all the required network devices, such as routers, switches, and end devices. 
</p> 
{{< figure src="../network_components.png" caption="Figure 2: Network components" >}}
<p style="text-align: justify;">
Packet Tracer provides both a logical and physical perspective, which is shown in Figure 3 and is located on the top left portion. The logical view is where you will spend the majority of your time configuring the network. Nevertheless, Packet Tracer also allows you to simulate networks based on geographic location (you can create cities or office at different location and connect) and also allows simulation of environmental data like temperature and soil moisture, as shown in Figure 4. In this hackathon, however, we will only work on logical mode.
</p>
{{< figure src="../logical_physical.png" caption="Figure 3: Network views" >}}
{{< figure src="../physical-env.png" caption="Figure 4: Environmental data" >}}

<p style="text-align: justify;">
	Now that we've examined the major Packet Tracer components, let's examine how to configure end devices and network components. To configure end devices or network components, click on the device, and a new configuration window will appear, as shown in Figure 5. Options vary depending on the types of network devices. Moreover, depending on the types of devices, additional features are also available. Figure 6 shows the additional options available for the end device, the desktop personal computer (PC).
</p>
{{< figure src="../config_details.png" caption="Figure 5: Configuration of end device" >}}
<p style="text-align: justify;"></p>

<p style="text-align: justify;"></p>
{{< figure src="../pc_details.png" caption="Figure 6: End device (PC) options" >}}






## Running Simulations
<p style="text-align: justify;">
You can test your network once it has been configured. Two modes are available for this in Packet Tracer, namely, Realtime and Simulation, as highlighted in Figure 7. 
</p>
{{< figure src="../simulation_mode.png" caption="Figure 7: Simulation modes" >}}
<p style="text-align: justify;">
	You can use the protocal data unit (PDU) by selecting it from the top left corner of the Packet Tracer user interface, as shown in Figure 8, to test your network connection (or run the ping command via a terminal or command prompt). Figure 9, for example, shows a test using PDU. In order to test the connectivity, follow the following steps: (i) select PDU; (ii) drop PDU at the source, which in our case is PC0; (iii) drop at the destination to which you want to test your connection, which in our case is Server0; and (iv) run the simulation. Figure 9 further shows the test run in simulation mode.
</p>
{{< figure src="../pdu_unit.png" caption="Figure 8: Protocol Data Unit" >}}

{{< figure src="../pdu_example.png" caption="Figure 9: Protocol Data Unit in action" >}}

<!-- <p style="text-align: justify;"></p>
<p style="text-align: justify;"></p> -->
{{< figure src="../simulation_test.png" caption="Figure 10:  Running test in simulation mode" >}}
<p style="text-align: justify;"></p>

## Getting Familiarization
<p style="text-align: justify;">
If you want to familiarize yourself with or practise, you can download the exercise file and work on it according to the provided instructions. Additionally, video solutions are provided below for your assistance.
</p>

- <a href="../ping_exercise.zip" download>Download the file for the first practise exercise</a>
- Solution
{{< youtube EEFwg9_SnX0 >}}
<br/>

- <a href="../ping_ii_router.zip" download>Download the file for the second practise exercise</a>
- Solution
{{< youtube DAvnvBs-gzg >}}


## Troubleshooting & Tips
<p style="text-align: justify;">
If you experience any issues, always check if everything is setup properly. For example, in the case of the router, you can use the command <i style="color: red;">show ip route</i> to see all the routes set in router command line interface (CLI), as shown in the Figure 11. 
</p>
{{< figure src="../cli.png" caption="Figure 10:  Running command in router CLI" >}}

<p style="text-align: justify;">
To configure using the CLI, you must first enable configuration mode. You can use the <i style="color: red;">config ter</i> or <i style="color: red;">config t</i> command. However, if you are unable to provde these commands, that means CLI is not enabled, which you can enable using <i style="color: red;">en</i> command. 
</p>


## Useful Resources

- [Cheatsheet Packet Tracer/Cisco](https://ocw.cs.pub.ro/courses/_media/rl/rl_cheatsheet.pdf)
- [Official Packet Tracer Tutorials](http://tutorials.ptnetacad.net/tutorials70.htm)
- [Computer Networking: a Top Down Approach, J.F. Kurose, K.W. Ross](https://gaia.cs.umass.edu/kurose_ross/index.php)
