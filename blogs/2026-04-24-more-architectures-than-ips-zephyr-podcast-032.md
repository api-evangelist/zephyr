---
title: "More Architectures Than IPs — Zephyr Podcast #032"
url: "https://www.zephyrproject.org/more-architectures-than-ips-zephyr-podcast-032/"
date: "Fri, 24 Apr 2026 21:54:15 +0000"
author: "Benjamin Cabé"
feed_url: "https://www.zephyrproject.org/feed/"
---
<p></p>
<ul>
<li>Yes, seriously: an IETF draft for <a href="https://www.ietf.org/archive/id/draft-thain-ipv8-00.html">IPv8</a></li>
<li>More Zephyr-adjacent goodness in Framework hardware, with <a href="https://www.youtube.com/watch?v=rgZlzCd0DUU&amp;t=1819s">ZMK</a> powering the new keyboard</li>
<li><a href="https://codeberg.org/hails/wsl9x">Windows 9x for Linux</a>, because running a Linux kernel as a Windows 95 application is apparently a thing</li>
<li>ST’s beefy <a href="https://www.st.com/en/microcontrollers-microprocessors/stm32h7r7-7s7.html">STM32H7RS</a> “boot flash enabled” Cortex-M7 MCU</li>
<li><a href="https://blog.adafruit.com/2026/04/21/porting-pebbleos-to-zephyr/">PebbleOS on Zephyr</a>, spotted via Adafruit</li>
<li><a href="https://github.com/shanteacontrols/opendeck">OpenDeck</a>, a Zephyr-based hardware and software platform for MIDI controllers</li>
<li>New processor architectures coming: <a href="https://github.com/zephyrproject-rtos/zephyr/pull/107516">TriCore</a> and <a href="https://github.com/zephyrproject-rtos/zephyr/pull/107122">Hexagon</a></li>
<li>A lightweight <a href="https://github.com/zephyrproject-rtos/zephyr/pull/107464">serial IPC backend</a> using COBS</li>
<li><a href="https://github.com/zephyrproject-rtos/zephyr/pull/106464">PTP IEEE 802.3 transport</a> support lands after a thorough review cycle</li>
<li><a href="https://github.com/zephyrproject-rtos/zephyr/pull/106359">HTTP/3</a> support follows up on the recently merged QUIC work</li>
<li>A proposed <a href="https://docs.google.com/document/d/1LpmsIbbjHpWGnjszRY1L7-0rWLly0gNDMwK_fA2YdBA/edit?tab=t.0">Robotics Working Group</a> for Zephyr</li>
<li>A <a href="https://github.com/zephyrproject-rtos/zephyr/issues/107078">kinematic tree subsystem RFC</a> for modeling robotics-style mechanical structures</li>
<li>Seeed Studio’s <a href="https://github.com/zephyrproject-rtos/zephyr/pull/107839">COB LED driver board</a> support</li>
<li><a href="https://github.com/zephyrproject-rtos/zephyr/pull/107542">Shell aliases</a> for taming long Zephyr shell command hierarchies</li>
<li>An overhaul of <a href="https://github.com/zephyrproject-rtos/zephyr/pull/107668">testplan discovery</a> on pull requests, with hopes for faster and more accurate CI</li>
<li>The e-ink-powered <a href="https://docs.zephyrproject.org/latest/boards/beagle/beaglebadge/doc/index.html">BeagleBadge</a> board</li>
<li><a href="https://github.com/zephyrproject-rtos/zephyr/pull/106941">CRSF remote controller support</a> for drones, rovers, and other robotics use cases</li>
<li>A native <a href="https://github.com/zephyrproject-rtos/zephyr/pull/105077">LoRaWAN backend</a>, including OTAA and Class A support</li>
<li>The <a href="https://docs.zephyrproject.org/latest/boards/shields/ad_apardpfw_sl/doc/index.html">AD-APARDPFW-SL</a> shield for single-pair Ethernet experiments</li>
<li><a href="https://github.com/zephyrproject-rtos/zephyr/pull/105258">ADP5360 PMIC</a> support, showing another nice multi-function device integration</li>
</ul>
<hr />
<p>Join Discord // #podcast at <a href="https://chat.zephyrproject.org/">https://chat.zephyrproject.org</a>!</p>
<p>Subscribe to the podcast on your favorite platform:</p>
<ul>
<li><a href="https://podcasts.apple.com/fi/podcast/the-zephyr-podcast/id1838016383">iTunes</a></li>
<li><a href="https://open.spotify.com/show/6N0DXmiPSSiGbPBfm2XkLw">Spotify</a></li>
<li><a href="https://link.deezer.com/s/310pixo4OMOCxlVzRRumh">Deezer</a></li>
<li><a href="https://antennapod.org/deeplink/subscribe/?url=%68%74%74ps%3A%2F%2Frss.libsyn.com%2Fshows%2F592130%2Fdestinations%2F5145420.xml&amp;title=The+Zephyr+Podcast">AntennaPod</a></li>
<li><a href="https://www.youtube.com/playlist?list=PLzRQULb6-ipFD-sMDAM8DZufKAobEWuEz">YouTube</a></li>
<li><a href="https://feeds.libsyn.com/592130/rss">RSS feed</a></li>
</ul>
<p>The summary below was automatically generated using the assistance of AI tools.</p>
<h2>Episode Summary</h2>
<section class="text-token-text-primary w-full focus:outline-none [--shadow-height:45px] has-data-writing-block:pointer-events-none has-data-writing-block:-mt-(--shadow-height) has-data-writing-block:pt-(--shadow-height) [&amp;:has([data-writing-block])&gt;*]:pointer-events-auto [content-visibility:auto] supports-[content-visibility:auto]:[contain-intrinsic-size:auto_100lvh] R6Vx5W_threadScrollVars scroll-mb-[calc(var(--scroll-root-safe-area-inset-bottom,0px)+var(--thread-response-height))] scroll-mt-[calc(var(--header-height)+min(200px,max(70px,20svh)))]" dir="auto">
<div class="text-base my-auto mx-auto pb-10 [--thread-content-margin:var(--thread-content-margin-xs,calc(var(--spacing)*4))] @w-sm/main:[--thread-content-margin:var(--thread-content-margin-sm,calc(var(--spacing)*6))] @w-lg/main:[--thread-content-margin:var(--thread-content-margin-lg,calc(var(--spacing)*16))] px-(--thread-content-margin)">
<div class="[--thread-content-max-width:40rem] @w-lg/main:[--thread-content-max-width:48rem] mx-auto max-w-(--thread-content-max-width) flex-1 group/turn-messages focus-visible:outline-hidden relative flex w-full min-w-0 flex-col agent-turn">
<div class="flex max-w-full flex-col gap-4 grow">
<div class="min-h-8 text-message relative flex w-full flex-col items-end gap-2 text-start break-words whitespace-normal outline-none keyboard-focused:focus-ring [.text-message+&amp;]:mt-1" dir="auto" tabindex="0">
<div class="flex w-full flex-col gap-1 empty:hidden">
<div class="markdown prose dark:prose-invert w-full wrap-break-word dark markdown-new-styling">
<section class="text-token-text-primary w-full focus:outline-none [--shadow-height:45px] has-data-writing-block:pointer-events-none has-data-writing-block:-mt-(--shadow-height) has-data-writing-block:pt-(--shadow-height) [&amp;:has([data-writing-block])&gt;*]:pointer-events-auto [content-visibility:auto] supports-[content-visibility:auto]:[contain-intrinsic-size:auto_100lvh] R6Vx5W_threadScrollVars scroll-mb-[calc(var(--scroll-root-safe-area-inset-bottom,0px)+var(--thread-response-height))] scroll-mt-[calc(var(--header-height)+min(200px,max(70px,20svh)))]" dir="auto">
<div class="text-base my-auto mx-auto pb-10 [--thread-content-margin:var(--thread-content-margin-xs,calc(var(--spacing)*4))] @w-sm/main:[--thread-content-margin:var(--thread-content-margin-sm,calc(var(--spacing)*6))] @w-lg/main:[--thread-content-margin:var(--thread-content-margin-lg,calc(var(--spacing)*16))] px-(--thread-content-margin)">
<div class="[--thread-content-max-width:40rem] @w-lg/main:[--thread-content-max-width:48rem] mx-auto max-w-(--thread-content-max-width) flex-1 group/turn-messages focus-visible:outline-hidden relative flex w-full min-w-0 flex-col agent-turn">
<div class="flex max-w-full flex-col gap-4 grow">
<div class="min-h-8 text-message relative flex w-full flex-col items-end gap-2 text-start break-words whitespace-normal outline-none keyboard-focused:focus-ring [.text-message+&amp;]:mt-1" dir="auto" tabindex="0">
<div class="flex w-full flex-col gap-1 empty:hidden">
<div class="markdown prose dark:prose-invert w-full wrap-break-word dark markdown-new-styling">
<ul>
<li>IPv8: An actual IETF draft for <a class="decorated-link" href="https://www.ietf.org/archive/id/draft-thain-ipv8-00.html" rel="noopener" target="_new">IPv8</a> is making the rounds, with the very serious idea of moving to 64-bit IP addresses.</li>
<li>ZMK in Framework Laptops: Framework’s latest keyboard work is powered by <a class="decorated-link" href="https://www.youtube.com/watch?v=rgZlzCd0DUU&amp;t=1819s" rel="noopener" target="_new">ZMK</a>, bringing another nice Zephyr-adjacent project into mainstream laptop hardware.</li>
<li>Windows 9x for Linux: <a class="decorated-link" href="https://codeberg.org/hails/wsl9x" rel="noopener" target="_new">wsl9x</a> runs a Linux kernel as a Windows 95 application, which is exactly as delightfully weird as it sounds.</li>
<li>STM32H7RS: ST’s <a class="decorated-link" href="https://www.st.com/en/microcontrollers-microprocessors/stm32h7r7-7s7.html" rel="noopener" target="_new">STM32H7RS</a> is a powerful Cortex-M7 MCU family built around the idea of booting from internal flash and running larger applications from external memory.</li>
<li>Zephyr on Pebble: A community project is exploring <a class="decorated-link" href="https://blog.adafruit.com/2026/04/21/porting-pebbleos-to-zephyr/" rel="noopener" target="_new">PebbleOS on Zephyr</a>, showing another fun path for bringing older embedded platforms back to life.</li>
<li>OpenDeck: <a class="decorated-link" href="https://github.com/shanteacontrols/opendeck" rel="noopener" target="_new">OpenDeck</a> is a Zephyr-based platform for building MIDI controllers, with support for wired MIDI, USB, Bluetooth, and custom hardware.</li>
<li>New Architectures: Work is underway to add <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/107122" rel="noopener" target="_new">Hexagon</a> and <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/107516" rel="noopener" target="_new">TriCore</a> architecture support to Zephyr, expanding into DSP and automotive-oriented use cases.</li>
<li>Serial IPC Backend: A new <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/107464" rel="noopener" target="_new">serial IPC backend</a> adds a COBS-based transport for communication between processors over serial links.</li>
<li>HTTP/3 and PTP: <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/106359" rel="noopener" target="_new">HTTP/3</a> support is already following the recent QUIC work, while <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/106464" rel="noopener" target="_new">PTP IEEE 802.3 transport</a> adds more time-sensitive networking capabilities.</li>
<li>Robotics in Zephyr: A proposed <a class="decorated-link" href="https://docs.google.com/document/d/1LpmsIbbjHpWGnjszRY1L7-0rWLly0gNDMwK_fA2YdBA/edit?tab=t.0" rel="noopener" target="_new">Robotics Working Group</a> and a <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/issues/107078" rel="noopener" target="_new">kinematic tree subsystem RFC</a> point to growing interest in making Zephyr a stronger platform for robotics.</li>
<li>Seeed COB LED Driver Board: Support for Seeed Studio’s <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/107839" rel="noopener" target="_new">COB LED Driver Board</a> led to a broader discussion about PWM examples and documentation.</li>
<li>Shell Aliases: <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/107542" rel="noopener" target="_new">Shell aliases</a> should make long Zephyr shell commands easier to use.</li>
<li>Testplan Discovery: A proposed <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/107668" rel="noopener" target="_new">testplan discovery overhaul</a> aims to make PR testing smarter, faster, and more relevant to the files that actually changed.</li>
<li>BeagleBadge: The <a class="decorated-link" href="https://docs.zephyrproject.org/latest/boards/beagle/beaglebadge/doc/index.html" rel="noopener" target="_new">BeagleBadge</a> brings Zephyr to a capable e-ink badge platform.</li>
<li>CRSF Remote Controller Support: <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/106941" rel="noopener" target="_new">CRSF input support</a> adds a protocol used by drones, rovers, and ExpressLRS-style remote-control systems.</li>
<li>Native LoRaWAN Backend: A native <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/105077" rel="noopener" target="_new">LoRaWAN backend</a> is in progress, starting with LoRaWAN 1.0.4, OTAA, Class A, and EU band support.</li>
<li>AD-APARDPFW-SL Shield: The <a class="decorated-link" href="https://docs.zephyrproject.org/latest/boards/shields/ad_apardpfw_sl/doc/index.html" rel="noopener" target="_new">AD-APARDPFW-SL</a> shield adds single-pair Ethernet experimentation to Zephyr.</li>
<li>ADP5360 PMIC: <a class="decorated-link" href="https://github.com/zephyrproject-rtos/zephyr/pull/105258" rel="noopener" target="_new">ADP5360 support</a> is a good example of Zephyr’s multi-function device model, exposing PMIC features such as charging, fuel gauge, GPIOs, and regulators.</li>
</ul>
</div>
</div>
</div>
</div>
</div>
</div>
</section>
</div>
</div>
</div>
</div>
</div>
</div>
</section>
