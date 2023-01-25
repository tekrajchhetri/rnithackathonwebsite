---
title: Task
date: '2023-01-22'
type: book
weight: 20
math: true
---


## Scenario
<p style="text-align: justify;">
You are a newly hired network engineer for a major corporation. The company is opening a new office in a different location and configuring the network so that all offices can connect seamlessly. Different engineers are located in various locations. You are responsible for setting up the network, including designing and configuring it at one of the locations, for example, Innsbruck. 

Using the provided Packet Tracer file, design and configure the network according to the outlined specifications.
</p>

- <a href="../hackathon_packet_tracer_file.zip" download>Download the Packet Tracer file</a>

## Requirements

 <p style="text-align: justify;">
 	<ul>
 		<li>Design a network with two autonomous systems (AS), namely, AS1 and AS2, and establish the connection between them. The AS1 should contain the three interconnected routers and the AS2, as shown in Figure 1. Further configuration instructions are provided below.
{{< figure src="../router.png" caption="Figure 1: Autonomous systems" >}}
<ul>
	<li> <b>AS1</b>
		<ul>
			<li><p style="text-align: justify;">Assign the number 1000 to AS1's AS number.</p></li>
			<li><p style="text-align: justify;">Assign the following names, RNITROUTERA, RNITROUTERB and RNITROUTERC, to the routers A, B, and C, respectively.</p></li>
		<li><p style="text-align: justify;">Configure the BGP protocol to connect to the AS2 and EIGRP for internal communication at the AS1. Use the following information to configure the routers:</p>
			<table class="table">
<thead>
  <tr>
    <th class="tg-1wig">SRC</th>
    <th class="tg-1wig"><span style="font-weight:700;font-style:normal">DST</span></th>
    <th class="tg-1wig"><span style="font-weight:700;font-style:normal">SRC IP</span></th>
    <th class="tg-1wig">DST IP</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">B</td>
    <td class="tg-0lax">D</td>
    <td class="tg-0lax">197.0.0.1</td>
    <td class="tg-0lax">197.0.0.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">B</td>
    <td class="tg-0lax">C</td>
    <td class="tg-0lax">194.0.0.2</td>
    <td class="tg-0lax">194.0.0.1</td>
  </tr>
  <tr>
    <td class="tg-0lax">B</td>
    <td class="tg-0lax">A</td>
    <td class="tg-0lax">195.0.0.2</td>
    <td class="tg-0lax">195.0.0.1</td>
  </tr>
  <tr>
    <td class="tg-0lax">C</td>
    <td class="tg-0lax">A</td>
    <td class="tg-0lax">193.0.0.1</td>
    <td class="tg-0lax">193.0.0.2</td>
  </tr>
</tbody>
</table>
<small>SRC: Source DST: Destination</small>
		</li>
<!-- 		<ul>
	<li><b>Router B:</b></li>
</ul> -->
 
</li>
		<li><p style="text-align: justify;">Connect a PC to the router A at 196.0.0.1.  Name the PC as STUDENTPC and assign the PC with the following IP address: 196.0.0.2.</p></li>
		<li> <p style="text-align: justify;">Create VLANs with the following configuration:</p>
			<table class="table">
<thead>
  <tr>
    <th class="tg-1wig">VLAN NAME</th>
    <th class="tg-1wig">VLAN NUMBER</th>
    <th class="tg-1wig">IP</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">INSTRUCTORS</td>
    <td class="tg-0lax">14</td>
    <td class="tg-0lax">192.168.40.5</td>
  </tr>
  <tr>
    <td class="tg-0lax">PRINTERS</td>
    <td class="tg-0lax">17</td>
    <td class="tg-0lax">192.168.60.5</td>
  </tr>
</tbody></table>
{{< callout note >}}
<p style="text-align: justify;">You need to configure inter-VLAN routing. In addition, remember to configure trunk and access ports appropriately.</p>
{{< /callout >}}
		</li>
		<li><p style="text-align: justify;">Connect two PCs to the VLAN INSTRUCTORS. One PC is labelled RNITINSTRUCTORS and has an IP address of 192.168.40.1; the second PC is labelled RNITADMIN and has an IP address of 192.168.40.2.</p></li>
		<li><p style="text-align: justify;">Connect a printer to the VLAN PRINTERS and assign the name RNITLABPRINTER and an IP address of 192.168.60.1 to the printer.</p></li>
		<li><p style="text-align: justify;">Two computers are connected physically to the router C via a switch. The switch should be named as RNITSWITCH. The first computer is named RNITLABPC1 and has an IP address of 192.168.30.5. The second computer, similarly, has the name RNITLABPC2 and an IP address of 192.168.30.6.</p></li>
	</ul>
	</li><br/>
{{< callout warning >}}
<p style="text-align: justify;">To enable communication between the end devices connected to routers C and A and the end device at the AS2, you must define the route. You can use the following command:</p>

`ip route 0.0.0.0 0.0.0.0 nexthop` 

Note: The configuration has to be done at routers C and A.
{{< /callout >}}
	<li> <b>AS2</b>
		<ul>
			<li>Assign the number 2000 to AS2's AS number.</li>
		<li><p style="text-align: justify;">Assign the router the IP address 197.0.0.2 and configure it to connect to router B from AS1 at 197.0.0.1 via the BGP protocol. </li>
		<li>Give the router the following name: RNITROUTERD.</li></li>
		<li><p style="text-align: justify;">Connect a PC to the router at the following IP address: 198.0.0.1. The PC should be named AS1PC and have an IP address of 198.0.0.2.</p></li><br/>
			{{< callout note >}}
The AS1PC at AS2 should be able to communicate with all the end devices at AS1.
{{< /callout >}}		
	</ul>
	</li>
</ul>

<li>Test all your connections to make sure you are able to communicate between AS1 and AS2 end devices.</li>
 	</ul>
</p>



## Useful Commands
You can use the following commands for the BGP and EIGRP protocols:
{{< callout note >}}
EIGRP configuration

`router eigrp ASNo`

BGP configuration

`router bgp ASNo`

Advertising routes

`network IP (subnet)`

Advertising neighbour 

`neighbor IP remoteASNo`
{{< /callout >}}
