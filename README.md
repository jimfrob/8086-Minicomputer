# 8086 Minicomputer
A basic minicomputer design based on the 8086 CPU

Before anyone starts poking holes in the massive gaps in the logic that Google's AI chat provided in the published documents, I have already started a Rev 2 version of this project to try to get it down to 100x100mm 2-layer boards (to make them ultra-cheap to order from PCBWay). While doing so, I uncovered MANY serious flaws in the design, including, but not limited to, the refresh timing for the DRAM. From here, I'll let my less-experienced self carry on.

Full disclosure up front: I heavily used LLM chats to help me with the design because I'm a complete noob. I just happened to have an 8086 8 MHz CPU lying about, as well as a Specialix I/O4+ quad UART serial card, and I thought I might like to build a minicomputer out of it. This idea was largely inspired by Usagi Electric's TMS9900 minicomputer project. You can check out his projects at https://github.com/Nakazoto

This is, as I've said, a minicomputer. It is my intention that one will only be able to communicate with it over serial terminal, and the serial card I have supports up to four. Storage will be handled by a fairly generic multi-I/O card built around the DLU 270. The eventual ROM code will have these cards in mind. Simply because it's what I have on hand that's 16-bit native, I've gone with the AM27C400 EPROM.

I'm providing the KiCad files I have developed for anyone to use, modify, whatever. I'm quite open to any helpful tips for improving the design. My only minor request is that anyone who makes changes makes sure those changes make it into the wild for everyone to enjoy.

There is absolutely no ROM code at the moment because I don't know any 8086 assembly. I'll be having to learn on the fly. Because of the sheer size of the EPROM, it's entirely possible that I may end up putting the whole OS in there, but this is still early days.
