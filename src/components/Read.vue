<script>
import Icons from './Icons';

export default {
  name: 'Read',
  components: {
    Icons,
  },
};
</script>
<style>
  @import '../assets/styles/style.css';
</style>
<template>
      <div class="root">
        <div class="ProjectView__Container-paxcuj-0 fRXRVr">
            <div class="ProjectContainer-s16s8y6k-0 kzFaUy">
                <div class="Project__ProjectWrapper-s1okt27x-0 dKLImk">
                    <div class="SpacedContent-s13gt09q-0 fOyKUT" id="TEDContent">
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 fqCFal" span="12">
                                        <div class="Text__InnerText-s1e82ayr-0 dbmxVQ" color="black">Applying the Unix <br>Process Model to Web Apps</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 bselgP">
                                        <div class="Text__InnerText-s1e82ayr-0 huZYeY">Tools</div>
                                        <div class="Text__InnerText-s1e82ayr-0 gquVkl"><span>React <span>Redux</span></span></div>
                                    </div>
                                    <div class="Col-mbuk5t-0 bselgP">
                                        <div class="Text__InnerText-s1e82ayr-0 huZYeY">Big Thing</div>
                                        <div class="Text__InnerText-s1e82ayr-0 gquVkl"><span>JSON Web Token Authentication</span></div>
                                    </div>
                                    <div class="Col-mbuk5t-0 bselgP">
                                        <div class="Text__InnerText-s1e82ayr-0 huZYeY">Demo</div>
                                        <div class="Text__InnerText-s1e82ayr-0 gquVkl"><a href="https://www.ted.com/attend/conferences/tedconnect" target="_blank" rel="noopener noreferrer" class="sc-bdVaJa fhxAte">Launch product</a></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 cZTvaB">
                                        <div class="Text__InnerText-s1e82ayr-0 ddvlSO">The unix process model is a simple and powerful abstraction for running server-side programs. Applied to web apps, the process model gives us a unique way to think about dividing our workloads and scaling up over time. Let’s begin with a simple illustration of the basics of the process model, using a well-known unix daemon: memcached.  </div>
                                        <div class="Text__InnerText-s1e82ayr-0 ddvlSO">Download and compile it:</div>
                                    </div>
                                    <div class="Col-mbuk5t-0 kXeKNk"></div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 cZTvaB">
                                        <div class="Image__Container-s1g7n88a-0 dWRovV">
                                            <picture>
                                                <source srcset="https://d2998a9lzvovjv.cloudfront.net/devices.1d2a5992.webp" type="image/webp">
                                                <source srcset="https://d2998a9lzvovjv.cloudfront.net/devices.03bb4866.png" type="image/png"><img src="https://d2998a9lzvovjv.cloudfront.net/devices.03bb4866.png" alt="ted devices">
                                            </picture>
                                        </div>
                                    </div>
                                    <div class="Col-mbuk5t-0 kXeKNk"></div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 cZTvaB">
                                        <div class="SpacedContent-s13gt09q-0 dTBSrq">
                                            <div class="Text__InnerText-s1e82ayr-0 egFFdI">Mapping the unix process model to web apps</div>
                                            <div class="Text__InnerText-s1e82ayr-0 ddvlSO">A server daemon like memcached has a single entry point, meaning there’s only one command you run to invoke it. Web apps, on the other hand, typically have two or more entry points. Each of these entry points can be called a process type.</div>
                                            <div class="Text__InnerText-s1e82ayr-0 ddvlSO">A basic Rails app will typically have two process types: a Rack-compatible web process (such as Webrick, Mongrel, or Thin), and a worker process using a queueing library (such as Delayed Job or Resque). For example</div>
                                        </div>
                                    </div>
                                    <div class="Col-mbuk5t-0 kXeKNk"></div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 cZTvaB">
                                        <div class="Image__Container-s1g7n88a-0 iCHCvU">
                                            <picture>
                                                <source srcset="https://d2998a9lzvovjv.cloudfront.net/network.71c31f4d.webp" type="image/webp">
                                                <source srcset="https://d2998a9lzvovjv.cloudfront.net/network.5414bcd7.png" type="image/png"><img src="https://d2998a9lzvovjv.cloudfront.net/network.5414bcd7.png" alt="ted network">
                                            </picture>
                                        </div>
                                    </div>
                                    <div class="Col-mbuk5t-0 kXeKNk"></div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 fNzIMd">
                                        <div class="SpacedContent-s13gt09q-0 dTBSrq">
                                            <div class="Text__InnerText-s1e82ayr-0 ieyKPK">Scaling a private social network</div>
                                            <div class="Text__InnerText-s1e82ayr-0 ddvlSO" color="onyx">How do you plan for spotty WiFi and unreliable 3G connections? We meticulously optimized response times and payload sizes to create a painless and seamless experience.</div>
                                        </div>
                                    </div>
                                    <div class="Col-mbuk5t-0 gsbdhK">
                                        <div class="Image__Container-s1g7n88a-0 dyMlAT">
                                            <picture>
                                            <source srcset="https://d2998a9lzvovjv.cloudfront.net/xcode.36c99ec3.webp" type="image/webp">
                                            <source srcset="https://d2998a9lzvovjv.cloudfront.net/xcode.4a8d0399.png" type="image/png"><img src="https://d2998a9lzvovjv.cloudfront.net/xcode.4a8d0399.png" alt="ted xcode"></picture>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="Container-ybirvx-0 eCMzjk">
                            <div>
                                <div class="Grid__GridContainer-xhz9es-0 TSGqh">
                                    <div class="Col-mbuk5t-0 cZTvaB">
                                        <div class="SpacedContent-s13gt09q-0 dTBSrq">
                                            <div class="Text__InnerText-s1e82ayr-0 egFFdI">The Results</div>
                                            <div class="Text__InnerText-s1e82ayr-0 ddvlSO" color="onyx">Business cards went the way of the dodo at TED: attendees shared over 7,000 contacts, created 155 locations, and checked in 3,685 times. TED Connect was used by over 65% of TED attendees (up from 14% with previous year's app) and TED has continued to use TED Connect at all of their conferences.</div>
                                        </div>
                                    </div>
                                    <div class="Col-mbuk5t-0 kXeKNk"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
