---
layout: post
title:  "Nixponetial growth"
date:   2024-02-24 16:22:00 -0500
categories: nix
---

I first got exposed to the power of nix while I was interning at Anduril in the summer of 2023. Since then I haven't really been able to get it off my mind. I had never really given a shit about package managers in the past and had only really cared about writing software to do shit. 

I write a lot of software for student competition teams and I work with several different groups in class and in my team throughout the course of a semester and with that comes the immense overhead of installing dependencies on everyone's machines or getting them setup with shitty VMs. This always takes way more time than it should and sometimes becomes a blocker for peeps to get involved in the project. Traditionally I know that minimizing deps for code is good practice but when I want to smash a bunch of shit together to get something working, speed for me trumps dependency avoidance. 

<img src="assets/images/image-1.png" alt="image" width="400" />

I am starting to get more into the Nix ecosystem and I feel like right now im at the peak of mount stupid:
<img src="assets/images/image.png" alt="image" width="400" />


cuz rn i feel emboldened to nixify everything and make everyone use it. However I am still pretty much illiterate when it comes to writing nix code and I am scared tho that the stuff im building for long term wont get looked at or grown once I leave since nix is still esoteric and the docs can be very sparse and aren't easily accessible. However, below is listed the stuff I have been reading for learning more about nix and nixos:

[https://artemis.sh/2023/06/06/cross-compile-nixos-for-great-good.html](https://artemis.sh/2023/06/06/cross-compile-nixos-for-great-good.html)

[https://stop-using-nix-env.privatevoid.net/](https://stop-using-nix-env.privatevoid.net/)

[https://flakehub.com/](https://flakehub.com/)

[https://zero-to-nix.com/](https://zero-to-nix.com/)

[https://www.jboy.space/blog/nix-on-hpc.html](https://www.jboy.space/blog/nix-on-hpc.html)

[https://rbf.dev/blog/2020/05/custom-nixos-build-for-raspberry-pis/](https://rbf.dev/blog/2020/05/custom-nixos-build-for-raspberry-pis/)

My background is mostly in embedded development and as such I am most comfortable in C++ in my day-to-day development. Along with this I have learned a lot about how to do CMake and in Nix it often feels like to me that there aren't a lot of people working on big C++ projects in nix (even though nix was written in C++). There exists native support for cmake builds but things like debugging and compile command generation are not part of the standard docs for a quick dev environment getting started in nix development. I also feel like the power of Nix could also be used in the land of firmware to truly accomplish amazing things.

most of the standard development tools exist [within Nix already](https://github.com/NixOS/nixpkgs/tree/master/pkgs/development/embedded) but from what I have seen only a handful of people have been using them.

prtzl made a dev [environment for stm32](https://github.com/prtzl/stm32) which is really interesting but I think things could get really interesting if embedded projects with multiple layers of hardware abstraction could be more easily composed and iterated on with the reproducibility that nix gives you pretty much for free and tools for large-scale firmware development. Tools like PlatformIO and the Arduino ecosystem provide many users already with a more traditional package management approach for firmware. if we had a section of nix packages or flakes on flakehub that wrapped firmware libraries and their build and flash environments we could go far. but what if we also brought the ability of nix to be a system configuration tool to the low-level micro-controller configuration like how stm32cube ide supports configuring chips? What if nix could talk in an [open register description language](https://peakrdl.readthedocs.io/en/latest/index.html) or use [CMSIS-SVD](https://github.com/cmsis-svd/cmsis-svd) files and parses? 

anywhomst, enough yapping about that, I just wanted to get that idea out of my head.


    