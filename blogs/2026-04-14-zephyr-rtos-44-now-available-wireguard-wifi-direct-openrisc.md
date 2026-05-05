---
title: "Zephyr RTOS 4.4 Now Available: WireGuard, Wi‑Fi Direct, OpenRISC, and More"
url: "https://www.zephyrproject.org/zephyr-rtos-4-4-now-available-wireguard-wi-fi-direct-openrisc-and-more/"
date: "Tue, 14 Apr 2026 21:33:50 +0000"
author: "Benjamin Cabé"
feed_url: "https://www.zephyrproject.org/feed/"
---
<div class="wpb_row vc_row-fluid vc_row" id="fws_69f2177957396" style="padding-top: 0px; padding-bottom: 0px;"><div class="row-bg-wrap"><div class="inner-wrap row-bg-layer"><div class="row-bg viewport-desktop"></div></div></div><div class="row_col_wrap_12 col span_12 dark left">
	<div class="vc_col-sm-12 wpb_column column_container vc_column_container col no-extra-padding inherit_tablet inherit_phone flex_gap_desktop_10px ">
		<div class="vc_column-inner">
			<div class="wpb_wrapper">
				
<div class="wpb_text_column wpb_content_element ">
	<p><span style="font-weight: 400;">On behalf of the Zephyr Project, I am thrilled to announce the general availability of </span><a href="https://github.com/zephyrproject-rtos/zephyr/releases/tag/v4.4.0"><span style="font-weight: 400;">Zephyr 4.4</span></a><span style="font-weight: 400;">—the first release under the project’s </span><a href="https://docs.zephyrproject.org/latest/releases/index.html#transitioning-to-the-new-release-cadence" rel="noopener" target="_blank"><strong>new bi-yearly release cadence</strong></a><span style="font-weight: 400;">. Moving to two major releases per year gives the community more time to mature each release and makes it easier for downstream projects to plan upgrades (one release in April, one in October, like Ubuntu!). This cycle brought <strong>contributions from over 930 individuals</strong>, delivering a release packed with significant networking improvements, support for a new processor architecture and much more.</span></p>
<p>As usual, I also recorded a demo video to accompany this article and show some of these features in action. Enjoy!</p>
</div>




	<div class="wpb_video_widget wpb_content_element vc_clearfix   vc_custom_1776098718148 vc_video-aspect-ratio-169 vc_video-el-width-80 vc_video-align-center">
		<div class="wpb_wrapper">
			
			<div class="wpb_video_wrapper"></div>
		</div>
	</div>

<div class="wpb_text_column wpb_content_element ">
	<p>Throughout the article, clicking the <img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /> symbol will take you to the relevant section of the video.</p>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=218s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Zephyr SDK 1.0 and C17</h2>
<p><span style="font-weight: 400;">Zephyr 4.4 is the first release to ship with </span><a href="https://docs.zephyrproject.org/latest/develop/toolchains/zephyr_sdk.html" rel="noopener" target="_blank"><strong>Zephyr SDK 1.0</strong></a> (1.0.1, to be precise!)<span style="font-weight: 400;">. The Zephyr SDK is a complete, standalone toolchain package that includes everything needed to build, flash, and debug Zephyr applications across all supported architectures and for all major operating systems (Windows, Linux, macOS). One of the most notable changes is the new experimental Clang/LLVM support, as well as the fact that it ships with pre-bundled versions of OpenOCD and QEMU for all operating systems.</span></p>
<p>This release also modernizes Zephyr’s C baseline by moving to <b>C17</b> (ISO/IEC 9899:2018) as the minimum required standard. While C17 was primarily a maintenance update, the transition allows the project to fully embrace modern <strong>C11</strong> features, such as <a href="https://www.gnu.org/software/c-intro-and-ref/manual/html_node/Static-Assertions.html">static assertions</a>, <code>_Generic</code> (type-generic macros), and more. Of course, the new SDK fully supports C17 but in case you&#8217;re tied to an older toolchain you can always force e.g. <code>CONFIG_STD_C99</code> as needed.</p>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=99s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> OpenRISC Architecture Support</h2>
<p><span style="font-weight: 400;">Zephyr 4.4 adds support for </span><a href="https://docs.zephyrproject.org/latest/boards/index.html#arch=openrisc" rel="noopener" target="_blank"><strong>OpenRISC</strong></a> (32-bit only for now)<span style="font-weight: 400;">, an open-source processor architecture popular in FPGA-based designs, academic research, and custom silicon applications. OpenRISC joins ARM, RISC-V, x86, Xtensa, ARC, MIPS, SPARC, and others in Zephyr’s already broad list of supported processor architectures.</span></p>
<p>If you’re working on open hardware or FPGA-based designs and have been looking for an RTOS to run on your OpenRISC cores, Zephyr is now an option worth considering.</p>
<h2>Secure, Direct Connectivity: Wi-Fi Direct and WireGuard VPN</h2>
<p>Two notable networking features land in Zephyr 4.4: <strong>Wi-Fi Direct</strong> support in the Wi-Fi management stack, and native <strong>WireGuard</strong> support.</p>
<h3><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=776s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Wi-Fi Direct (P2P)</h3>
<p><span style="font-weight: 400;">The Wi-Fi management stack now supports </span><a href="https://docs.zephyrproject.org/latest/connectivity/networking/api/wifi.html#wifi-mgmt-p2p" rel="noopener" target="_blank"><strong>Wi-Fi Direct (P2P)</strong></a><span style="font-weight: 400;">, allowing devices to discover and connect to each other directly—without a traditional access point. Think device provisioning in the field, peer-to-peer data synchronization, or direct sensor-to-gateway communication in environments where infrastructure Wi-Fi is unavailable or impractical. Wi-Fi Direct supports multiple security modes, including WPA2-PSK and WPA3-SAE.</span></p>
<h3><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=445s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> WireGuard VPN</h3>
<p><span style="font-weight: 400;"><img alt="" class="alignright wp-image-24614 " height="72" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/wireguard-logo.png" width="406" />The networking stack also gains support for </span><a href="https://docs.zephyrproject.org/latest/samples/net/wireguard/README.html" rel="noopener" target="_blank"><strong>WireGuard VPN</strong></a><span style="font-weight: 400;">, enabling secure, low-overhead tunneling directly on your Zephyr devices. WireGuard is known for its simplicity, speed, and strong cryptography, making it an ideal fit for resource-constrained embedded devices that need secure remote management or encrypted data transport.</span></p>
<p><span style="font-weight: 400;">Check out the </span><a href="https://docs.zephyrproject.org/latest/samples/net/wireguard/README.html" rel="noopener" target="_blank"><span style="font-weight: 400;">sample application</span></a><span style="font-weight: 400;"> that&#8217;s available to get a sense of the (very few!) configuration options you need to enable WireGuard in your application.</span></p>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=1151s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> USB Host Expansion: Cameras and More</h2>
<p><span style="font-weight: 400;">Experimental USB host support has been significantly expanded in Zephyr 4.4 with a new host-class driver framework and support for </span><strong>UVC (USB Video Class) cameras</strong><span style="font-weight: 400;"> on Zephyr devices acting as USB hosts.</span></p>
<p>This opens the door to embedded vision scenarios that pair really well with the networking additions above. Once it becomes possible to connect virtually any webcam to a Zephyr-based device, it is easy to imagine building systems that capture a video feed and then expose or tunnel it over a direct peer-to-peer connection or a VPN link.</p>
<p><span style="font-weight: 400;">Interestingly, this release also adds a number of new video camera sensor drivers, including for the <strong>Himax HM0360</strong>, <strong>OmniVision OV5642 and OV7675</strong>, and the <strong>Sony IMX219</strong> (the sensor at the heart of the Raspberry Pi Camera Module 2</span><span style="font-weight: 400;">).</span></p>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=2073s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Pressure-Based CPU Frequency Scaling</h2>
<p><span style="font-weight: 400;">Building on the </span><a href="https://docs.zephyrproject.org/latest/services/cpu_freq/index.html" rel="noopener" target="_blank"><span style="font-weight: 400;">CPU frequency scaling</span></a><span style="font-weight: 400;"> subsystem introduced in Zephyr 4.3, this release adds a new </span><a href="https://docs.zephyrproject.org/latest/services/cpu_freq/index.html#pressure-policy" rel="noopener" target="_blank"><strong>pressure-based policy</strong></a><span style="font-weight: 400;"> that automatically adjusts CPU frequency according to scheduler load. The policy monitors &#8220;<strong>system pressure</strong>&#8221; by observing the number of threads currently in the <b>ready queue</b> and their relative priorities. When the queue lengthens or higher-priority tasks are waiting, the system ramps up the clock for responsiveness; when the load subsides, it scales back to save power.</span></p>
<p><span style="font-weight: 400;">For battery-powered devices that occasionally need <strong>bursts of performance</strong>—think handling sensor data, processing network packets, or running ML inference—this kind of intelligent frequency scaling can help extend battery life without sacrificing real-time responsiveness. This is just one example of a scaling policy built into Zephyr, and it is straightforward to implement your own if you want to account for additional factors (system temperature anyone?).</span></p>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=2386s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> ARM Cortex-M Context Switching Performance</h2>
<p><span style="font-weight: 400;">A new context switch implementation for ARM Cortex-M, enabled via <code>CONFIG_USE_SWITCH</code>, delivers significant performance improvements.</span></p>
<p>When running the standard <a href="https://github.com/zephyrproject-rtos/zephyr/tree/main/tests/benchmarks/thread_metric"><code>thread_metric</code></a> benchmark, an average 8% speed improvement is observed. Given that ARM Cortex-M is Zephyr&#8217;s most popular architecture family, this change provides a meaningful boost to a large number of applications!</p>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=1260s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> New Driver Classes</h2>
<p><span style="font-weight: 400;">Zephyr 4.4 introduces several new driver APIs, expanding the types of hardware that it can natively support:</span></p>
<ul>
<li style="font-weight: 400;"><strong><a href="https://docs.zephyrproject.org/latest/hardware/peripherals/otp.html" rel="noopener" target="_blank">One-Time Programmable (OTP) Memory</a></strong><span style="font-weight: 400;"> – A new API for provisioning and reading permanent device data such as calibration values, secure keys, and device identifiers. Drivers are available for NXP OCOTP, STM32 BSEC, Sifli eFuse, and more. OTP devices can also be accessed through the </span><a href="https://docs.zephyrproject.org/latest/services/storage/nvmem/nvmem.html" rel="noopener" target="_blank"><span style="font-weight: 400;">NVMEM subsystem</span></a><span style="font-weight: 400;">.</span></li>
<li style="font-weight: 400;"><strong><a href="https://docs.zephyrproject.org/latest/hardware/peripherals/biometrics.html" rel="noopener" target="_blank">Biometrics</a></strong><span style="font-weight: 400;"> – A new API for integrating biometric sensors such as fingerprint scanners or facial recognition systems. This enables new product categories ranging from biometric access control to secure authentication on embedded devices. Initial drivers support the ADH-Tech GT5x and Zhiantec ZFM-x0 fingerprint sensors.</span></li>
<li style="font-weight: 400;"><strong><a href="https://docs.zephyrproject.org/latest/hardware/peripherals/wuc.html" rel="noopener" target="_blank">Wake-up Controller (WUC)</a></strong><span style="font-weight: 400;"> – A new API for managing wake-up sources that can bring the system out of low-power states, providing finer-grained control over power management behavior.</span></li>
</ul>
<h2><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=1907s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Zbus Proxy Agents: Multi-Core Messaging</h2>
<p>Zephyr’s <a href="https://docs.zephyrproject.org/latest/services/zbus/index.html" rel="noopener" target="_blank">zbus</a> publish-subscribe message bus now supports <a href="https://docs.zephyrproject.org/latest/doxygen/html/group__zbus__proxy__agent.html" rel="noopener" target="_blank"><strong>proxy agents</strong></a> that can forward channel traffic across CPU and domain boundaries over IPC. This makes it possible to use zbus&#8217; high-level messaging API in potentially complex multi-core scenarios without having to use low-level, sometimes error-prone IPC APIs.</p>
<p><span style="font-weight: 400;">The setup is straightforward: define a proxy agent, create shadow channels, and let zbus handle the forwarding:</span></p>
<p><!-- HTML generated using hilite.me --></p>
<div style="background: #ffffff; overflow: auto; width: auto; border: solid gray; border-width: .1em .1em .1em .8em; padding: .2em .6em;">
<pre style="margin: 0; line-height: 125%;">ZBUS_PROXY_AGENT_DEFINE(proxy_agent, ZBUS_PROXY_AGENT_BACKEND_IPC, IPC_DEV_NODE);
ZBUS_CHAN_DEFINE(sensor_data, <span style="color: #00f;">struct</span> <span style="color: #2b91af;">sensor_msg</span>, NULL, NULL, ZBUS_OBSERVERS_EMPTY, ZBUS_MSG_INIT(0));
ZBUS_PROXY_ADD_CHAN(proxy_agent, sensor_data);</pre>
</div>
<p><span style="font-weight: 400;">A new </span><a href="https://docs.zephyrproject.org/latest/samples/subsys/zbus/zbus-proxy-agent-ipc/README.html" rel="noopener" target="_blank"><span style="font-weight: 400;">sample application</span></a><span style="font-weight: 400;"> demonstrates the full setup.</span></p>
<h2>Developer Experience Improvements</h2>
<p>As always, several quality-of-life improvements made it into this release. In no particular order:</p>
<h3><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=1639s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Build Dashboard</h3>
</div>




	<div class="wpb_gallery wpb_content_element clearfix">
		<div class="wpb_wrapper"><div class="wpb_gallery_slidesflickity_static_height_style"><div class="nectar-flickity not-initialized instace-69f217795b5ad"><div class="flickity-viewport"> <div class="flickity-slider"><div class="cell"><img alt="" class="skip-lazy nectar-lazy attachment-large" height="615" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/Screenshot-2026-04-13-at-21.36.50-1024x615.png" title="Screenshot 2026-04-13 at 21.36.50" width="1024" /></div><div class="cell"><img alt="" class="skip-lazy nectar-lazy attachment-large" height="615" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/Screenshot-2026-04-13-at-21.37.01-1024x615.png" title="Screenshot 2026-04-13 at 21.37.01" width="1024" /></div><div class="cell"><img alt="" class="skip-lazy nectar-lazy attachment-large" height="615" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/Screenshot-2026-04-13-at-21.37.35-1024x615.png" title="Screenshot 2026-04-13 at 21.37.35" width="1024" /></div><div class="cell"><img alt="" class="skip-lazy nectar-lazy attachment-large" height="615" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/Screenshot-2026-04-13-at-21.37.41-1024x615.png" title="Screenshot 2026-04-13 at 21.37.41" width="1024" /></div><div class="cell"><img alt="" class="skip-lazy nectar-lazy attachment-large" height="615" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/Screenshot-2026-04-13-at-21.37.51-1024x615.png" title="Screenshot 2026-04-13 at 21.37.51" width="1024" /></div></div></div></div></div>
		</div> 
	</div> 
<div class="wpb_text_column wpb_content_element ">
	<p><span style="font-weight: 400;">A new </span><a href="https://docs.zephyrproject.org/latest/develop/optimizations/tools.html#dashboard" rel="noopener" target="_blank"><strong><code>dashboard</code></strong></a><span style="font-weight: 400;"> build target consolidates a wealth of build information into a single interactive HTML report. RAM and ROM footprint (as drill-down tables and sunburst charts), Kconfig symbol values and their sources (from <code>traceconfig</code>, introduced in Zephyr 4.3), initialization levels, and a navigable Devicetree view with property values and binding details—all in one place.</span></p>
<div style="background: #ffffff; overflow: auto; width: auto; border: solid gray; border-width: .1em .1em .1em .8em; padding: .2em .6em;">
<pre style="background: #fff !important; margin: 0; line-height: 125%;">west build -p -b &lt;board&gt; samples/hello_world -t dashboard
</pre>
</div>
<p><span style="font-weight: 400;">The generated report opens up automatically in your browser <img alt="🙂" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/1f642.png" style="height: 1em;" /> If you’ve been running <code>ram_report</code>, <code>rom_report</code>, <code>traceconfig</code>, and similar tools separately, this will undeniably save you time.</span></p>
<h3>Heap Hardening</h3>
<p>A new tiered heap hardening system (enabled and configured through <code><a href="https://docs.zephyrproject.org/latest/kconfig.html#CONFIG_SYS_HEAP_HARDENING" rel="noopener" target="_blank">CONFIG_SYS_HEAP_HARDENING</a></code>) adds runtime corruption detection to <code>sys_heap_alloc</code> and <code>sys_heap_free</code>.</p>
<p>In many ways, heap corruption can get even nastier than your classical stack overflow. A buffer overflow that writes past the end of an allocation silently clobbers the size metadata of the next chunk; a double-free leaves the free list in an inconsistent state; a stale pointer writes into memory that&#8217;s already been returned to the heap; etc. In all of these cases, the allocator operates on corrupted data, and the failure surfaces somewhere completely unrelated, often much later.</p>
<p>The four levels of hardening go all the way from &#8220;basic&#8221; double-free and overflow detection (with a negligible runtime cost) to complete validation of the heap structure after every allocation and free operation (which you would likely only use when debugging due to the massive overhead!).</p>
<p><!-- IMAGE: Screenshot of the Zephyr build dashboard showing RAM/ROM sunburst charts, Kconfig trace, and Devicetree view --></p>
<h3><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=2512s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Scope-Based Cleanup Helpers (RAII/defer for C)</h3>
<p><span style="font-weight: 400;">One of the most common sources of bugs in embedded C code is forgetting to release a resource—unlocking a mutex, freeing memory, closing a file handle—especially in code paths with early returns. Zephyr 4.4 introduces </span><a href="https://docs.zephyrproject.org/latest/kernel/cleanup.html" rel="noopener" target="_blank"><strong>scope-based cleanup helpers</strong></a><span style="font-weight: 400;"> that bring RAII/defer-style automatic cleanup to C.</span></p>
<p><span style="font-weight: 400;">For example, here’s how you can use a scoped guard to automatically lock and unlock a mutex:</span></p>
<div style="background: #ffffff; overflow: auto; width: auto; border: solid gray; border-width: .1em .1em .1em .8em; padding: .2em .6em;">
<pre style="background: #fff !important; margin: 0; line-height: 125%;"><span style="color: #333;">static</span> K_MUTEX_DEFINE(lock);

<span style="color: #333;">void</span> <span style="color: #06b; font-weight: bold;">critical_section</span>(<span style="color: #333;">void</span>)
{
	scope_guard(k_mutex)(&amp;lock);

	<span style="color: #888;">// Lock is held here</span>
	<span style="color: #888;">// Perform critical operations</span>

	<span style="color: #888;">// Lock is automatically released when scope exits,</span>
	<span style="color: #888;">// even on early return!</span>
}
</pre>
</div>
<p><span style="font-weight: 400;">The API also supports scoped variables (auto-init and cleanup), scoped defers (for arbitrary cleanup functions), and works with all code paths including early returns, breaks, and gotos. Enable it with <code>CONFIG_SCOPE_CLEANUP_HELPERS</code>.</span></p>
<h3><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=2659s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> Ztest Benchmarking Framework</h3>
<p><span style="font-weight: 400;">Writing performance benchmarks for embedded code has traditionally been ad-hoc and inconsistent. Zephyr 4.4 adds a new </span><a href="https://docs.zephyrproject.org/latest/develop/test/benchmark.html" rel="noopener" target="_blank"><strong>ztest benchmarking framework</strong></a><span style="font-weight: 400;"> that provides a standardized way to create cycle-accurate benchmarks with automated data collection, overhead compensation, and statistical reporting (mean, standard deviation, min/max). Use the familiar <code>ZTEST_BENCHMARK()</code> macro, and get publication-quality performance data out of the box.</span></p>
<h3><a href="https://www.youtube.com/watch?v=KoMIB980bpU&amp;t=1461s" rel="noopener" target="_blank"><img alt="▶" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/25b6.png" style="height: 1em;" /></a> QEMU Display Driver</h3>
<div class="wp-caption aligncenter" id="attachment_24626" style="width: 527px;"><img alt="" class="wp-image-24626" height="413" src="https://www.zephyrproject.org/wp-content/uploads/2026/04/Screenshot-2026-04-13-at-22.44.31-1024x818.png" width="517" /><p class="wp-caption-text" id="caption-attachment-24626">LVGL demo app running on qemu_x86 on macOS</p></div>
<div>A new display driver for QEMU targets simplifies the development of display-based applications in environments where the native simulator is unavailable or not always practical to use. If you’re building a graphical interface and want to iterate quickly without physical hardware, this is a lifesaver.</div>
<h2>And more!</h2>
<p><span style="font-weight: 400;">Catch up on the full </span><a href="https://docs.zephyrproject.org/latest/releases/release-notes-4.4.html" rel="noopener" target="_blank"><span style="font-weight: 400;">release notes</span></a><span style="font-weight: 400;"> and don&#8217;t forget the </span><a href="https://docs.zephyrproject.org/latest/releases/migration-guide-4.4.html" rel="noopener" target="_blank"><span style="font-weight: 400;">migration guide</span></a><span style="font-weight: 400;"> that documents the steps you need to take to update your Zephyr 4.3-based code.</span></p>
<p><span style="font-weight: 400;">Enjoy this new release, come and say hi on </span><a href="https://chat.zephyrproject.org" rel="noopener" target="_blank"><span style="font-weight: 400;">Discord</span></a><span style="font-weight: 400;"> if you have questions, feedback, or would like to get involved. Finally, check out the <a href="https://www.youtube.com/channel/UCohVfwDfzCZ_gh3DvIZ4fJA/">Zephyr YouTube channel</a> and <a href="https://zephyrpodcast.libsyn.com/">Zephyr Podcast</a> to not miss future news!</span></p>
</div>




			</div> 
		</div>
	</div> 
</div></div>
