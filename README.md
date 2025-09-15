(if you have a better name pls create an issue xd)
<h1 align="center"> Project "Portable Router" </h1>

> [!WARNING] 
> i'm **NOT** responsible for the damage that this process could cause to your hardware. do this at your own risk and be prepared to debug, and debug a lot. in case you aren't familiar with basics of linux cli, OpenWRT / forks and networking - take your time, this will be hard. you have been warned.

---

### content
<details>
<summary> table of content </summary>

1. Disclaimer 
2. Requirements
3. Current tested devices
4. Contribution
5. "But why?" or Reasons
6. P.S.
</details>

### structure:
in `doc/` we have `.md` files for routers tested;
in `src/` we have images and etc for text;

<h2 align="center"> Disclaimer </h2>

!!! **read WARNING once more** !!! and this:
1. if you haven't tried OpenWRT / LEDE / etc - **read how to use it**. this repo **is not** a OpenWRT support forum!
2. if you have zero / close to zero experience in networking - **do your research first**. this repo **is not** a networking 101!
3. do **not** create issues like "Help my <routername> is bricked!" or "Will it work with <routername>?". do your research first! **OR**
4. if you want to **Contribute** - read how first! 
5. and lastly - it's **not** a "budget-friendly router build"! (although some pocket-sized routers are cheap) it's all about **portable** routers.  


<h2 align="center"> Requirements </h2>

mostly "Requirements" comes down to four things:
1. router itself 
2. modem 
3. power bank
4. SIM-card with internet

**however**, there are things to consider:
- your router **must** be on *OpenWRT* (or fork)
- your modem **must** support *mobile carrier aggregation*
- your power bank **must** provide enough power. e.g. my current setup w/ Cudy TR30 and Fibocom L850 consumes about 15W in a peak, that means my power bank must be at least 20W with PD on port

optionally, you can have:
- VPS for wg/proxy hosting
- switch for expanding amount of Ethernet ports
- USB extension cord 
- Physical eSIM

<h2 align="center"> Current Tested Devices </h2>

| Image | Status | Link | Author |
| - | - | - | - | 
| <img src="https://www.cudy.com/cdn/shop/files/TR1200.png" width="250">  | Working; Small amount of RAM and not so fast CPU, stable branch; | [Here](./doc/routers/cudy/TR1200.md) | hand7s |
| <img src="https://www.cudy.com/cdn/shop/files/TR3000.png" width="250"> | Working; 128mb revision is preferred since it's on a stable branch; | [Here](./doc/routers/cudy/TR3000.md) | hand7s |
| - | - | - | - |
| <img src="https://www.fibocom.com/uploadfiles/2022/04/20220413101231199.png" width="250"> | Requiers workaround; Cat.9, medoicre speed, any SIM / eSIM works fine | [Here](./doc/modems/l850gl.md) | hand7s |
| <img src="https://cdn.techship.com//uploads/images/1698/10919_190425.png" width="250"> | Requiers workaround; Cat.16, good speed, any SIM / eSIM works fine | [Here](./doc/modems/l850gl.md) | hand7s 

<h2 align="center"> Contribution </h2>

to expand list above you need to:
1. create an issue with "add router" template
2. go trough testings (with help from community ofc)
3. fork **this** repo with branch's name of your router, e.g. `xiaomi_ax3200`
4. write an `.md` in `doc/routers/` directory in a respected directory, e.g. `doc/cudy/TR3600.md`
5. add your router to [this](./doc/content.md) `.md` 
6. open a PR!

p.s.
you can init a modem with you router btw

<h2 align="center"> But.. Why? </h2>

this is a healthy question considering whole idea, but you might misunderstood why i've started this in a first place. 
most of ISPs are garbage. anywhere in the world you'll pay a lot for bare minimum, sometimes even [security holes](https://youtu.be/TFolQUeWoog?si=tX3JFeQKcmBawhtt) in your ISP, and even if you pay premium - stability still an option, not a requirement. one day i said "enough" and got into this project.
yet, mobile carriers not all rainbows and unicorns - various prices, various features, questionable contracts. but you can easily swap mobile carrier since it's just a SIM (or, if you'll buy physical eSIM, just a carrier) and not a whole big process of changing ISP, and way cheaper. and you are **NOT** forced to use crappy ISP hardware.
and there are more benefits:
1. you can use Modem as your backup / second ISP via [mwan](https://openwrt.org/docs/guide-user/network/wan/multiwan/mwan3)
2. you can use PPR (yes, it's a PPR in a short) as a second / backup router itself

but the main feature for this project - being **off-grid**. 
having this little thing in you backpack and giving yourself a part of private internet with your **own** rules (WG, OVPN, Proxy, Provider) anywhere in the world (with right setup). just pull this thing out of backpack and use it in a public cafe and use your internet by cable for your laptop. or Wi-Fi, if you brave enough. you can even have a working WIRED internet while driving / on a train, if you catch a signal. and if signal is GOOD - aggregation kicks in. possibilities are numeros.

in general, you *could* try this with any branded router and random USB modem stick, but idea of PPR is not only "Router + Modem". it's a "efficient portable router on a OpenWRT firmware with USB modem that supports mobile carrier aggregation". 

i hope this answers question "why".

<h2 align="center"> P.S. </h2>

huge thanks to [Askhat](https://github.com/Askhalion) for helping me with this

we are available at:

[GitHub](https://github.com/s0me1newithhand7s/ProjectPortableRouter)

[Forgejo](https://git.hand7s.org/s0me1newithhand7s/ProjectPortableRouter)

---

[![staaaaars](https://api.star-history.com/svg?repos=s0me1newithhand7s/PortableRouterProject=Date)](https://www.star-history.com/#s0me1newithhand7s/PortableRouterProject&Date)