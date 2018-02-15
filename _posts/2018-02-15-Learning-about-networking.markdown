---
layout: post
title:  "Learning about networking"
date:   2018-02-15 10:38:35 +1100
categories: jekyll update
---
Today I got a quick overview of how public addresses work. Before I type anything, let me clear up that I'M NOT AN EXPERT IN THE SUBJECT, and if you know about how networking works chances are you know more than me, so if anything I wrote is wrong feel free to let me know, twitter handle's down the bottom.

So without further ado, let me tell you what I learnt today about networking. A long long time ago, when computers weren't at the palm of our hands but actually more used for scientific research, some US government dudes just really wanted to communicate better (probably between each other for war reasons but don't quote me on that), so a bunch of scientist got together and created this network of networks we'd eventually call... 
{% highlight ruby %}
THE INTERNET.
{% endhighlight %}
So, the internet was created, that was pretty great, but for people to connect to it they'd need to follow the TCP/IP (Transmission Control Protocol/Internet Protocol), and get a lil public number assigned to their machine so everyone could find eachother. Kinda like I need a house address to <s>stalk</s>find my friends, a computer would need an IP address so others could find them on the internet. So when someone wanted to get connected to the internet, they got a public IP address! (Don't ask me who gave it to them I don't quite know that)

Eventually, after giving public IP addresses out like candy on halloween, ICANN (Internet Corporation for Assigned Names and Numbers, I think the title is self-explanatory enough) got worried. "Guys, if we just give a public IP to everyone, won't we eventually run out of IPs to give?", said someone, which when I think about it it's totally strange because from my understanding they'd have around 4.3 billion public IP adresses back then, so either this guy had pretty good foresight of how many machines there would be now, or I'm just underestimating how many machines there were back then. Regardless, everyone was like "Yeah alright that's probably a good idea".

They came up with a few IP addresses that would be "private", that meant that no one could PUBLICLY access that address. This VIP club of private addresses was named RFC1918. Apparently this is just a very brief overview of course, but the 3 IP ranges I was taught to be private are:
<ul>
<li>192.168.0.0/16</li>
<li>172.16.0.0/10</li>
<li>10.0.0.0/8</li>
</ul>
(Oh, and don't worry about the /(number), I'll explain that in a few lines.)
That means if anyone trying to publicly find an IP address that uses those numbers is gonna have a bad time. They're hidden from the public.
<img src="../_imgs/networking/hidden.jpg">

"But Pedro why is this important, the number of addresses are still the same right?"
Kind of, but not really. Public IP adresses are still limited, but multiple computers can have the same private IP adresses in different networks because there's no way. I kinda think of it as multiple appartments. No building can have the same adress, that's impossible. However, more than one building can have the same unit numbers. There can be hundreds or people living on the fourth floor on apt 420, but they all live in different buildings. I can have the address 192.168.0.1, and so can someone else, as long as we don't do it inside the same private network. Again, grossly simplifying things but that's what I understood from it.

That also affects how you connect to the internet at home, all your machines use 1 public address graciously given to you by your ISP, and each of your machines has a different private address to connect to it. They all connect to a gateway (Usually your router). Your router has public interface that gives you a public IP address, but inside your house all machines are connected internally privately.
<img src="../_imgs/networking/isp.jpg">

Meaning that, networks that are local, for example working in a wonderful company like MYOB, you can use those private IP addresses within it's network. You can have the IP 192.168.0.122 or something, because you're using it internally. And other computers on that internal network can also see you! Like I said, it's like a VIP party, no one on the outside is invited, and everyone on the inside is having heaps of fun. 
There are certain numbers that cannot be used, whether they are private like I talked about, or they are reserved for things like "boradcast" or "this" (Don't ask me what these are I just heard the terms). 
<img src="../_imgs/networking/gateway.jpg">

Right, before we finish, the /(numbers), and how IP addresses are formed. If you were to look at an IP address, chances are you are looking at a pattern similar to this:
{% highlight ruby %}
XXX.XXX.XXX.XXX
{% endhighlight %}
Where X can be subsituted for numbers and it can have either 1 or 3 Xs between each dots. But actually, IP addresses are binary, represented like this:
{% highlight ruby %}
11111111.11111111.11111111.11111111
{% endhighlight %}
Where each 1 can either be a 1 or a 0. Now, I'm not going to explain binary but it's real easy if you have a good teacher, and I'm sure there are some good binary tutorials out there on the net. Either way, those 8 1/0s can make up numbers from 0 to 255 (Which is why there can only be 1 to 3 XXXs!). That's 32 1/0s in total.
"So why do I need to know the binary part of this?"
Well, thats because the /(number) relates to that. It refers to the number of BINARY houses your network can "edit", meaning that if you are using
192.168.0.0/16
<ul>
<li>The 192.168 is FIXED, and every IP inside that network will have those numbers. Meaning there are 16 FIXED Binary houses being used.</li>
<li>The 0.0 is NOT FIXED, meaning you can edit them. Meaning there are 16 NOT FIXED Binary houses for use. Hence, the /16.</li>
<li>16+16 = 32, meaning all numbers are used.</li>
</ul>


To be more clear:
192.168 in binary is equal to 11000000.10101000. You can see there are 16 1/0s there right?
And the 255.255 is equal to 11111111.11111111, which also is 16 1/0s.
<img src="../_imgs/networking/binary.jpg">

I hope this was entertaining and/or useful, but that's it for today. Again, I'm still learning a lot of things, so if you have anything that you want me to correct, add or even articles/books to read, just give me a lil tweet, my twitter is at the bottom of the page. Till next time!

Pedro.

