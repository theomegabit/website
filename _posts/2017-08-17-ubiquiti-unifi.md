---
layout: post
title: "Review: Ubiquiti Unifi"
date: 2017-08-25
banner_image: ubiquiti1.png
tags: [review, wireless, networking, ubiquiti, unfi, accesspoint, wifi]
---

There are a multitude of wireless routers, hubs, and switches aimed at the consumer market. And while the higher end may have enough features to please even more picky power users and “techies”, there’s something to be said about choices, particularly prosumer choices. One such company that falls under that category is Ubiquiti. They’ve been around for awhile to be fair. But, over time they’re continued to build upon the previous generation’s successes and keep moving forward. The team over at Ubiquiti was nice enough to send over a nice assortment of goodies including their Gateway/firewall, 8 port switch, Cloud Controller key, and an AC Pro access point.

We’ve been using the gear for the last ~6 weeks and have a fairly good assortment of thoughts. And there are a lot of them…

<!--more-->


## Software

Hardware is still important in 2016. But more often than not, hardware lifespans can be extended with good hardware. Not to mention, poor software can shorten hardware’s lifespans. In the case of Ubiquiti, they make some pretty nice software both in terms of functionality and features as well as UI. In fact, the UI is one of my favorite aspects of it. The way it lays out data from end to end is nice, clean and generally simple without being dumbed down. That said, to make the most of the software and monitoring, you really need Ubiquiti device at every step of the way. Without a link in the chain, while nice, it just isn’t as full featured and “pretty” to look at.

Setting up the Ubiquiti hardware devices and cloud controller for the first time can be a bit frustrating. And this is perhaps the greatest hurdle Ubiquiti would have to address if they wanted to push down into more “normal” consumer spaces. Specifically, I already had a single AC Pro setup with the cloud controller software setup on a mac mini on my network. In the process of setting up the environment with the hardware based cloud controller key from Ubiquiti, I had an incredibly tough time getting the original AP I had to disassociate with the original controller. In theory it’s not supposed to be hard at all. But in my experience it just wouldn’t let the past go. I eventually got so frustrated with it I walked away and came back a few hours later and voila… it was ready to join the new cloud controller.

{% include image_full.html imageurl="/images/posts/unifidashboard.jpg" title="Unifi Dashboard" caption="Unifi Dashboard" %}

Once that slight aggravation was settled things got a lot easier and what one would expect. While items within the various pages and menus aren’t the most detailed out there, they’re good enough for the prosumer space in my opinion. Along the same lines, it can be a bit confusing at first to have to jump between selecting each hardware device to see configuration settings for each piece of hardware as they aren’t configurable globally in a single place. Meanwhile, other settings *can* be configured in a more global menu. Needless to say, while it’s certainly easier than setting up some Cisco gear via command line, it’s not quite to the level of your typical router you’d buy at Best Buy. Really, I’d say it’s on par with Meraki in terms of layout with some minor differences between the two in what is placed where.

Cons aside, the software will do a ton. Everything from mutli-VLANing your networks to point-to-point VPNs (which is rather easy to setup) makes the Ubiquiti environment incredibly versatile and something that nerds will enjoy tinkering with. And of course, my favorite part is the interface that will detail a lot of different metrics about what is currently going on within your network including everything between connected devices to bandwidth. For chart junkies the Ubiquiti ecosystem’s interface is something worth exploring.

All that said, one area I wish Ubiquiti would improve on is the cloud management. For starters, the reliance on local software running on a computer or the dedicated hardware “key” seems like a weird crutch. I’d like to see it moved all to the cloud like Meraki’s solution. It’s simply one less complication to deal with.

Overall, I’d rate the software more than acceptable. While it can take a bit of learning and getting used to (especially if you’re moving from consumer to prosumer),  it is slightly more approachable than Cisco/Meraki on both price and learning curve standpoints. And to recap, I like charts… and colors. And when you have end-to-end components that all talk nicely together, it makes for a pretty great experience.

## AC Pro
{% include image_full.html imageurl="/images/posts/unifi-acpro.jpg" title="Unifi AC Pro" caption="Unifi AC Pro" %}

Specs:

* 3 x Dual-band antennas, 2.4 GHz: 3 dBi, 5 GHz: 6 dBi
* 802.11a/b/g/n/ac w/ band steering
* weather resistant
* Passive Power over Ethernet (48 V), 802.3af/803.2at Supported
* (Supported Voltage Range: 44 to 57 VDC)
* Max power consumption: 9 W
* Supported speeds:
    * 802.11a
    * 6, 9, 12, 18, 24, 36, 48, 54 Mb/s802.11n
    * 6.5 to 450 Mb/s (MCS0 – MCS23, HT 20/40)802.11ac
    * 6.5 to 1300 Mb/s (MCS0 – MCS9 NSS1/2/3, VHT 20/40/80)802.11b
    * 1, 2, 5.5, 11 Mb/s802.11g
    * 6, 9, 12, 18, 24, 36, 48, 54 Mb/s


The AC Pros are perhaps one of the nicest looking yet simple APs we’ve come across. The white disk with center glowing circle seems very Apple-like in simplicity. The glowing circle pulls double duty, too, as an indicator of the APs status between no connected clients, connected clients, errors/issues, etc.

On the underside are just a few ports – a power port, an ethernet port and a secondary ethernet port to daisy chain APs together. Being that the AC Pros support standard PoE (power over ethernet) — and not that 24v passive junk which is annoying — you’re best option to reduce clutter and unnecessary wires is make sure you have a switch that also supports PoE. The 8 port switch by Ubiquiti just happens to have said support, though any PoE switch will work. You can sit the AC Pro flat as well as mount it on a wall or ceiling with the provided mount.

One other nice perk: the AC Pros are weather resistant enough that you can legit mount them outside without any special covering or case. So, for those of you looking to extend your network to a detached building or simply cover the backyard in modern wireless goodness, the barrier to doing that is much lower. All you need is some Cat 5 cable run to the location of the AP and said AP. The software will then step in and give you an easy way to add and extend to your network.

Over the last few months I’ve had a solid experience. There has been a single instance in which the AP needed a reboot but other than that, coverage has been great, speeds high, and the experience very much “set it and forget it” after the initial grief. I will admit I was skeptical at first regarding range with the AC Pro vs. some of the other routers I have which feature much larger, external antennas. Generally speaking, the larger the antenna the better range you’ll get. Now, I’m not a hardware engineer so I’m not going to pretend I know exactly how or why something with smaller internal antennas on this prosumer device can match (and at times exceed) the ranage of something, say, [like this](https://www.engadget.com/2015/01/05/d-link-wifi-routers-powerline/). Just know that the AC Pro can. It needs to be said though, wireless is a fickle thing and your experience could (and very likely will) vary.

## Unifi AC Mesh

{% include image_right.html imageurl="/images/posts/unifimesh.jpg" title="Unifi AC Mesh points" caption="Unifi AC Mesh points" %}

Truth be told, these mesh points from Ubiquiti are actually much newer than the other gear in the review here. But over time as I've continued using the Unifi gear, it's been a welcome addition to further bolster network coverage and versatility with the two additional mesh points.

The way the work is much like any other repeater. The dual-band AC units can be both wired and wireless added to your network.

Even in wireless mode, I didn't see any noticeable differences in speed or performance when several devices were connected to both the mesh point and the downstream wireless uplink AP. In a real world, high speed test however, the performance degradation when multiple hops are involved cannot be forgotten or discounted. In the scope of a normal sized house, it's not something you'll likely have to worry about.

## Switch & Firewall/Gateway

Switch hardware these days is honestly kind of boring. It’s the software features that make the HW intriguing and differentiate one device from the next. As we touched on earlier, Ubiquiti’s software is quite nice to look at and only gets better the more Ubiquiti devices you have running together. And that is the big kicker here – to truly get the best experience you really need to have as much Ubiquiti hardware as possible.

With the switch and gateway one is able to literally control just about anything, and all via a wonderful GUI that brings networking into the modern world so you can get in, do what you need, and get out.

Spec wise the switch and gateway are what you would expect – multiple 1 gig ports all providing standard PoE for any other PoE devices you might want to plug into it.

* (8) Gigabit RJ45 Ports
* (2) SFP Ports
* Non-Blocking Throughput: 10 Gbps
* Switching Capacity: 20 Gbps
* Forwarding Rate: 14.88 Mpps
* Maximum Power Consumption: 150W
* Supports POE+ IEEE 802.3at/af and 24V Passive PoE
* Quiet, Fanless Operation
* Rackmountable with Rack-Mount Brackets (Included)
* Desktop-Mountable(DonotphysicallystacktheUS-8-150W.)

Much the same as the switch, the gateway is a great addition to any network as it is a more business-y security gateway. That is, it actively works toward protecting your network to intrusions from the outside. Some of the more notable specs include:

* (3) 10/100/1000 RJ45 Ports*
* (1) RJ45 Serial Console Port
* Quiet, Fanless Operation
* Wall?Mounting Capability
* Layer 3 Forwarding Performance

## Heat

While most of the discussion’s we’ve had with others regarding Ubiquiti hardware has been almost unanimously positive we have had people chat with us regarding component quality. While I can’t speak for the quality of the components (outside my expertise) I will say that I never had any issues with the units Ubiquiti sent. To be fair, ~4 months isn’t a great length in the true “long term review” spectrum. Nonetheless, the ambient temperature in the building I have been in was quite warm (~80-87) during the middle of summer. Yes, the Ubiquiti hardware has been running hot, maybe even “wow, that’s hot for a gadget” (specifically, the gateway got the hottest). But they haven’t so much as blinked in the higher operating temps they’ve been subjected to. And for that I can at least say I’m appreciative. Perhaps in 12 months we’ll see how things are still fairing. Maybe they’ll throw up a white flag in 18 months. For now, though, all I can say is that I have not had any issues with them. I’m pleased with how the hardware has performed.

## Wrap-up
{% include image_right.html imageurl="/images/posts/ubiquiticlose.png" title="Unifi" caption="Unifi" %}
The vast majority of people are going to spring for something cheap from Best Buy. And that’s fine. Most people don’t want or need the features that Ubiquiti or any other pro-sumer/business level hardware and software provides. But for those who do, Ubiquiti is a great option to consider compared to one of the other big names in this space – Meraki (by Cisco). While Meraki is a more fleshed out and truly enterprise level product, it also 1) costs more and 2) can be more involved, especially if you delve into the more traditional Cisco namespace.

I would say most anyone considering this setup almost certainly can figure out some of the software gripes I had early on. It was annoying but not a show stopper. That said, it also highlighted another area that Cisco (and frankly, many other consumer level hardware) has an advantage over – community and support. The community around Ubiquiti is very vocal and loyal, but it’s also small. There’s no way around it – the community is simply small, which makes finding answers to questions a little more involved and time consuming. Add to that the lack of deeper documentation into the hardware/software and you have the recipe for a headache when problems pop up, especially if you’re not the type of person who is ok with rolling up their sleeves and getting their hands dirty.

Initial setup and HW quality concerns aside, my time with the various pieces of hardware has been largely non-eventful. And really, that’s what you want. Set it and forget it. When you need to change something, get in, change it and get out while also being able to get a good look at your network when you want to dig deeper thanks to the great reporting and charting of various metrics.

If you’re looking to get into the pro-sumer space for your home or even small business, Ubiquiti is worth a look. The lower cost of entry to other options means it’s approachable and a much lower risk if it ends up not being a right fit down the road.

<div align="center">A big thank you to Ubiquiti who was kind enough to send all this gear over.</div>
