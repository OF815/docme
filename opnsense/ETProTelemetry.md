<div class="rst-content">
          <div role="navigation" aria-label="Page navigation">
  <ul class="wy-breadcrumbs">
      <li><a href="../index.html" class="icon icon-home" aria-label="Home"></a></li>
      <li class="breadcrumb-item active">ET Pro Telemetry edition</li>
      <li class="wy-breadcrumbs-aside">
      </li>
  </ul>
  <hr>
</div>
          <div role="main" class="document" itemscope="itemscope" itemtype="http://schema.org/Article">
           <div itemprop="articleBody">
             
  <div class="section" id="et-pro-telemetry-edition">
<h1>ET Pro Telemetry edition<a class="headerlink" href="#et-pro-telemetry-edition" title="Permalink to this heading"></a></h1>
<p>Todays cybersecurity engineers need timely and accurate data about eminent threats and how they spread around the globe.
With this data cybersecurity researchers and analysts can improve the detection of malicious network traffic.
The times when we could rely on just firewall rules for our protection are long gone.
Additional layers of security are desperately needed to guard against these attacks.</p>
<p>With growing risks the need to fortify our security is growing for both big enterprises as for SMEs alike, but often
out of reach for the latter.
An important extra security addition is an Intrusion Detection and Prevention System (IDS/IPS).</p>
<p>The IDS/IPS available in OPNsense is based on Suricata.
This open source IDS/IPS engine has proven its value in OPNsense, especially in combination with the free Proofpoint ETOpen ruleset.</p>
<p>The need for valuable threat detection data and the increasing importance of additional network security
has brought Proofpoint and OPNsense together.
Our joined efforts resulted in the ET Pro Telemetry edition.</p>
<p>The ET Pro Telemetry edition embraces our vision that sharing knowledge leads to better products.</p>
<p>When you allow your OPNsense system to share anonymized information about detected threats - the alerts -
you are able to use the ET Pro ruleset free of charge.</p>
<blockquote>
<div><p><em>The ET Pro ruleset is updated daily and covers more than 40 different categories of network behaviors,
malware command and control, DoS attacks, botnets, informational events, exploits, vulnerabilities,
SCADA network protocols, exploit kit activity, and more. If offers a great improvement over the ET open ruleset.</em></p>
</div></blockquote>
<div class="section" id="product-information">
<h2>Product information<a class="headerlink" href="#product-information" title="Permalink to this heading"></a></h2>
<p>For more information about emerging threats ETPro including the Telemetry edition, please visit their discord available at <a class="reference external" href="https://community.emergingthreats.net/">https://community.emergingthreats.net/</a>.
The following links are likely of interest:</p>
<ul class="simple">
<li><p><a class="reference external" href="https://community.emergingthreats.net/c/announcements/5">Announcements/Updates</a></p></li>
<li><p><a class="reference external" href="https://community.emergingthreats.net/c/feedback-support/8">Feedback/Support</a></p></li>
<li><p><a class="reference external" href="https://community.emergingthreats.net/c/tutorials-tips-tricks/13">Tutorials/Tips/Tricks</a></p></li>
</ul>
</div>
<div class="section" id="registration">
<h2>Registration<a class="headerlink" href="#registration" title="Permalink to this heading"></a></h2>
<p>When you register for this (free) service, you will share your basic (company) details with us, Deciso Sales B.V..
We will register your sensor(s) anonymized at Proofpoint.</p>
<div class="admonition note">
<p class="admonition-title">Note</p>
<p>When ET Pro Telemetry is activated, your OPNsense system sends data to Proofpoint. Proofpoint does not know who you are, they
only know how many sensors an account owns. Your network statistics received by Proofpoint won’t be shared with us.</p>
</div>
<p>Sign up for ET Pro Telemetry edition <a class="reference external" href="https://shop.opnsense.com/">here</a></p>
</div>
<div class="section" id="installation">
<h2>Installation<a class="headerlink" href="#installation" title="Permalink to this heading"></a></h2>
<p>After registration, we can proceed to the installation steps, which are described below.</p>
<div class="admonition note">
<p class="admonition-title">Note</p>
<p>To use ET Pro Telemetry, you will need to have OPNsense 19.1 or higher installed. When using an older version,
please upgrade to the latest first.</p>
</div>
<div class="section" id="plugin">
<h3>plugin<a class="headerlink" href="#plugin" title="Permalink to this heading"></a></h3>
<p>First we need to install the required plugin, which is responsible for collecting the telemetry data and provides access
to the ET Pro ruleset.</p>
<ol class="arabic simple">
<li><p>Go to <span class="menuselection">System ‣ Firmware ‣ Updates</span></p></li>
<li><p>press “Check for updates” in the upper right corner.</p></li>
<li><p>open the tab “Plugins” and search for <cite>os-etpro-telemetry</cite></p></li>
<li><p>when found, click on the [+] sign on the right to install the plugin</p></li>
</ol>
<p>A screen containing the installation status should appear now and the plugin is ready for use.</p>
</div>
<div class="section" id="register-token">
<h3>register token<a class="headerlink" href="#register-token" title="Permalink to this heading"></a></h3>
<p>Next step is to register your token in OPNsense and enable rulesets.</p>
<ol class="arabic simple">
<li><p>Go to <span class="menuselection">Services ‣ Intrusion Detection ‣ Administration</span></p></li>
<li><p>Click on the “Download” tab, which should show you a list of available rules.</p></li>
<li><p>Enable all categories you would like to monitor in the “ET telemetry” section,
if in doubt enable all and monitor the alerts later (select on the right and use the enable selected button on top)</p></li>
<li><p>At the bottom of the page there’s a block containing settings, paste the token code you received via email in <strong>et_telemetry.token</strong></p></li>
<li><p>Press <strong>save</strong> to persist your token code</p></li>
<li><p>Press <strong>Download &amp; Update rules</strong> to fetch the current ruleset</p></li>
</ol>
</div>
<div class="section" id="schedule-updates">
<h3>Schedule updates<a class="headerlink" href="#schedule-updates" title="Permalink to this heading"></a></h3>
<p>To download the rulesets automatically on a daily bases, you can add a schedule for this task.</p>
<ol class="arabic simple">
<li><p>Go to <span class="menuselection">Services ‣ Intrusion Detection ‣ Administration</span></p></li>
<li><p>Click on the “Schedule” tab</p></li>
<li><p>A popup for the update task appears, enable it using the checkbox on top, and click “save changes”</p></li>
</ol>
</div>
<div class="section" id="subscription-status">
<h3>Subscription status<a class="headerlink" href="#subscription-status" title="Permalink to this heading"></a></h3>
<p>To validate your subscription, we recommend to add the widget to the dashboard.</p>
<ol class="arabic simple">
<li><p>Go to the dashboard <span class="menuselection">Lobby ‣ Dashboard</span></p></li>
<li><p>Click on “Add widget” in the top right corner, click “Telemetry status” in the list</p></li>
<li><p>Close dialog and click “Save settings” on the right top of the dashboard</p></li>
<li><p>Open <span class="menuselection">Lobby ‣ Dashboard</span> again to refresh the content</p></li>
</ol>
<p>When everything is setup properly and the plugin can reach Proofpoint, it will show something like:</p>
<img alt="../_images/ETPRO_telemetry_widget_active.png" src="../_images/ETPRO_telemetry_widget_active.png">
<p>The status determines which ruleset your sensor will receive, <strong>ACTIVE</strong> or <strong>DORMANT</strong> your sensor will receive ET Pro ruleset,
when <strong>DISABLED</strong> the license conditions are not met and the ET Open ruleset will be served.</p>
<p>All timestamps underneath the status provide you with information when data was send or received from Proofpoint.</p>
<div class="admonition note">
<p class="admonition-title">Note</p>
<p>If your sensor will start sending events and heartbeats, it should switch to active after a certain amount of time.</p>
</div>
<p>In case your sensor can’t communicate to the outside world, the widget shows an error.</p>
<img alt="../_images/ETPRO_telemetry_widget_error.png" src="../_images/ETPRO_telemetry_widget_error.png">
<div class="admonition note">
<p class="admonition-title">Note</p>
<p>The system log (<span class="menuselection">System ‣ Log Files ‣ General</span>) might contain more information, search for <em>emergingthreats</em></p>
</div>
<div class="admonition tip">
<p class="admonition-title">Tip</p>
<p>Always check the token code first, a common mistake is adding leading or trailing spaces to the code, which will
show an error in the log (http_code starting with a 4 usually).</p>
</div>
</div>
</div>
<div class="section" id="information-sent-to-proofpoint">
<h2>Information sent to Proofpoint ©<a class="headerlink" href="#information-sent-to-proofpoint" title="Permalink to this heading"></a></h2>
<p>When the intrusion detection system logs events, they will be (partially) sent to Proofpoint in return for using the
ET Pro Telemetry edition.</p>
<p>This paragraph describes the attributes from the
<a class="reference external" href="https://suricata.readthedocs.io/en/suricata-4.1.0/output/eve/eve-json-format.html">eve.json</a> log file
that are collected to improve threat detection and the sensor health data to evaluate if the data is usable.</p>
<p>An example of an event is detailed below.</p>
<div class="highlight-json notranslate"><div class="highlight"><pre><span></span><span class="p">{</span>
<span class="w">  </span><span class="nt">"event_type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"alert"</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"proto"</span><span class="p">:</span><span class="w"> </span><span class="s2">"IPV6-ICMP"</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"timestamp"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2018-04-17T18:38:04.498109+0200"</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"in_iface"</span><span class="p">:</span><span class="w"> </span><span class="s2">"em1"</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"alert"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">    </span><span class="nt">"category"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Generic Protocol Command Decode"</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"severity"</span><span class="p">:</span><span class="w"> </span><span class="mi">3</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"rev"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"gid"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"signature"</span><span class="p">:</span><span class="w"> </span><span class="s2">"SURICATA zero length padN option"</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"action"</span><span class="p">:</span><span class="w"> </span><span class="s2">"allowed"</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"signature_id"</span><span class="p">:</span><span class="w"> </span><span class="mi">2200094</span>
<span class="w">  </span><span class="p">},</span>
<span class="w">  </span><span class="nt">"src_ip"</span><span class="p">:</span><span class="w"> </span><span class="s2">"xxxx:xxxx:fec0:d65f"</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"flow_id"</span><span class="p">:</span><span class="w"> </span><span class="mi">982154378249516</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"dest_ip"</span><span class="p">:</span><span class="w"> </span><span class="s2">"ff01:fe00:1200:8900:0000:f000:0000:0016"</span>
<span class="p">}</span>
</pre></div>
</div>
<p>Network addresses are needed to identify hosts which pose a higher risk to your and other peoples network, but your internal
addresses are kept secret.</p>
<p>For this reason we mask the addresses found in the log file and only send the last number(s) to identify the host.
In the example above the <em>src_ip</em> is an internal IPv6 address, for IPv4 we only collect the last number (e.g. 0-255).</p>
<p>Fields collected (unmodified):</p>
<hr class="docutils">
<div class="wy-table-responsive"><table class="docutils align-default">
<colgroup>
<col style="width: 21%">
<col style="width: 79%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p>timestamp</p></td>
<td><p>Timestamp of the event</p></td>
</tr>
<tr class="row-even"><td><p>flow_id</p></td>
<td><p>Internal identifier for this communication flow</p></td>
</tr>
<tr class="row-odd"><td><p>in_iface</p></td>
<td><p>Interface where the event was captured</p></td>
</tr>
<tr class="row-even"><td><p>event_type</p></td>
<td><p>Type of event</p></td>
</tr>
<tr class="row-odd"><td><p>vlan</p></td>
<td><p>Vlan tag</p></td>
</tr>
<tr class="row-even"><td><p>src_port</p></td>
<td><p>Source port number</p></td>
</tr>
<tr class="row-odd"><td><p>dest_port</p></td>
<td><p>Destination port number</p></td>
</tr>
<tr class="row-even"><td><p>proto</p></td>
<td><p>Protocol</p></td>
</tr>
<tr class="row-odd"><td><p>alert</p></td>
<td><p>Alert details, such as the signature_id, action taken
and associated message.</p></td>
</tr>
<tr class="row-even"><td><p>tls</p></td>
<td><p>TLS details, such as certificate subject and serial.</p></td>
</tr>
<tr class="row-odd"><td><p>http</p></td>
<td><p>HTTP detail information such as the host, but omitting
sensitive details such as path and user-agent.</p></td>
</tr>
<tr class="row-even"><td><p>app_proto</p></td>
<td><p>Application protocol (if known)</p></td>
</tr>
</tbody>
</table></div>
<p><em>Threats change often, to keep statistics valuable, the list of fields is subject to change</em></p>
<div class="admonition note">
<p class="admonition-title">Note</p>
<p>The plugin comes with a small script to print eve output yourself, it’s called <strong>dump_data.py</strong>, when used with the <strong>-p</strong>
parameter, it will output the data as it will be sent to Proofpoint.
All script code can be found in the following directory <em>/usr/local/opnsense/scripts/ids_telemetry/</em></p>
</div>
<p>Sensor health status collected and send as keep-alive:</p>
<hr class="docutils">
<div class="wy-table-responsive"><table class="docutils align-default">
<colgroup>
<col style="width: 31%">
<col style="width: 69%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p>Unique Sensor ID</p></td>
<td><p>Unique sensor identification, helps identifying messages from the same system,
without knowing who is the operator.</p></td>
</tr>
<tr class="row-even"><td><p>OPNSense Version</p></td>
<td><p>Current installed software version.  This will help both for troubleshooting purposes
(if a bad update is pushed and Proofpoint notices that deployments running version
X have an issue) as well for planning, to understand how new features and
functionality would be adopted.</p></td>
</tr>
<tr class="row-odd"><td><p>Suricata Version</p></td>
<td><p>Suricata version installed.</p></td>
</tr>
<tr class="row-even"><td><p>Suricata status</p></td>
<td><p>Reports if the sensor is active, when not active, no detection/telemetry can be provided.</p></td>
</tr>
<tr class="row-odd"><td><p>System Time</p></td>
<td><p>If the system time is not correct, it will impact the timestamps of messages,
so knowing what time the system thinks it has will help reconcile the actual time.</p></td>
</tr>
<tr class="row-even"><td><p>Active Ruleset Version</p></td>
<td><p>The active ruleset version should match what is published.
If sensors do not have the active version then they either haven’t configured
scheduled updates or there is another issue.
This will help Proofpoint to identify if there are widespread issues with updates.</p></td>
</tr>
<tr class="row-odd"><td><p>Number of rules enabled</p></td>
<td><p>Helps to gain a better understanding about the number of rules people use on top of
the ones provided by Proofpoint.</p></td>
</tr>
<tr class="row-even"><td><p>Number of ETPro Telemetry Rules enabled</p></td>
<td><p>Because users can control what rules they enable,
they may not want to enable all ETPro Telemetry rules,
if this is the case it would help Proofpoint understand how the rules are being
leveraged so they can better write / tune rules</p></td>
</tr>
<tr class="row-odd"><td><p>Mode (IDS or IPS)</p></td>
<td><p>This is helpful to understand how the system is deployed and is useful to
development purposes to determine what rules we should be focusing on based
on how our customers are using them.</p></td>
</tr>
<tr class="row-even"><td><p>Suricata Log Stats</p></td>
<td><p>For QA purposes, some fields with general stats are collected
from /var/log/suricata/stats.log (capture.kernel_packets, decoder.pkts, decoder.bytes,
decoder.ipv4, decoder.ipv6, flow.tcp, flow.udp, detect.alert)</p></td>
</tr>
</tbody>
</table></div>
</div>
</div>


           </div>
          </div>
          <footer>

  <hr>

  <div role="contentinfo">
    <p>© Copyright 2016-2024, Deciso B.V.</p>
  </div>

  Built with <a href="https://www.sphinx-doc.org/">Sphinx</a> using a
    <a href="https://github.com/readthedocs/sphinx_rtd_theme">theme</a>
    provided by <a href="https://readthedocs.org">Read the Docs</a>.
   

</footer>
        </div>
