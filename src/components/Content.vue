<script>
import helpers from '../helpers/random';
import Icons from './Icons';
import projectsJson from '../data/projects.json';
import workJson from '../data/work.json';
import extrasJson from '../data/extras.json';

export default {
  name: 'Content',
  components: {
    Icons,
  },
  data() {
    const data = {
      projects: projectsJson,
      work: workJson,
      num: 0,
      extras: extrasJson,
      whatwewants: ['rootcomponent', 'project1', 'project2', 'project3', 'project4'],
      whatwewant: 'rootcomponent',
      links: {
        project1: [
          'project1',
          'project2',
          'project3',
          'project4',
          'project5',
        ],
        project2: [
          'project2',
        ],
        project3: [
          'project3',
        ],
        project4: [
          'project4',
        ],
        project5: [
          'project5',
        ],
      },
    };

    data.project1Link = helpers.getRandomFromArray(data.links.project1);
    data.project2Link = helpers.getRandomFromArray(data.links.project2);
    data.project3Link = helpers.getRandomFromArray(data.links.project3);

    return data;
  },
  computed: {
    featuredProject() {
      return this.projects.find(obj => obj.featured === true);
    },
  },
  methods: {
    onProject1Click() {
      //this.project1Link = helpers.getRandomFromArray(this.links.project1);
      this.whatwewant = 'project1';
    },
    onProject2Click() {
      this.project2Link = helpers.getRandomFromArray(this.links.project2);
    },
    onProject3Click() {
      this.project3Link = helpers.getRandomFromArray(this.links.project3);
    },
    // onProjectClick() {
    //   let project = this.projects.find(obj => obj.number === 1);
    //   let num = project.number;
    //   // console.log(num);
    //   this.whatwewant = this.whatwewants[num];

    // },
    onHomeClick() {
      this.whatwewant = 'rootcomponent';
    },
  },
};
</script>
<template>
  <div class="content-wrapper" v-if="whatwewant === 'rootcomponent'">
    <section>
      <h2>Projects</h2>
      <p v-for="paragraph in featuredProject.longDescription">{{paragraph}}</p>
      <div 
        class="project" 
        v-for="project in projects" 
        v-if="!project.hidden"
        v-on:click="number = project.number">
        <h3>
          <a :href="project1Link" v-on:click="onProject1Click()" target="_blank">{{project.title}}</a> 
        </h3>
        <p>{{project.description}}</p>
        <p class="project-links" v-on:click="onProject1Click()">
          <a class="HeaderMini__BackButton-s19m3osg-0 gzEtTD sc-bwzfXH ilLFvv" >
            <div class="Button__ButtonContent-s1ov6wwx-0 jnPIJs" format="outline">
              <div>
                <div class="Icon__IconContainer-s1eymix-0 clAVox" role="img">
                  <svg class="Icon-s1eymix-2 kALlyJ" width="20" height="20" viewBox="0 0 20 20"><g fill-rule="evenodd"><path transform="rotate(45 4.001 12.985)" d="M5.364 -0.236H7.364V15.764H5.364z"></path><path transform="scale(1 -1) rotate(45 54.613 2.021)" d="M5.364 9.764H7.364V25.764H5.364z"></path><path d="M2 14H26V16H2z" transform="translate(3 1)"></path></g></svg>
                </div><span class="p_small">&nbsp;Read More</span>
              </div>
            </div>
          </a>
        </p>
      </div>
    </section>

    <section class="featured-project bg-accent-light" v-if="featuredProject">
      <h2>Featured Project</h2>
      <p v-for="paragraph in featuredProject.longDescription">{{paragraph}}</p>
    </section>

    <section class="about">
      <h2>About</h2>
      <p>
        I work as a Senior Software Engineer at <a href="https://etsy.com" target="_blank">Etsy</a> in New York, and I’ve been 
        active in the engineering world for over 6 years.
      </p>
      <p>
        I was lucky enough to have a supportive mother, who got me thalida.com 
        for my 16th birthday. It was one of the best gifts I’ve ever received, 
        and is the reason I've become the developer I am today.
      </p>
      <p>
        I now work with an amazing team during the day, and in the wee hours of 
        the night I hack away at one of my many side projects. I'm always 
        looking for a coding buddy, so if you're interested, get in touch! 
      </p>
      <p>
      </p>
    </section>
    <section class="work">
      <h2>Work History</h2>
      <div 
        class="job" 
        v-for="job in work" 
        v-if="!job.hidden">
        <h3 class="job-header">
          <span class="job-company">{{job.company}}</span>
          <span class="job-duration">{{job.duration}}</span>
        </h3>
        <p class="job-title">{{job.title}}</p>
      </div>
    </section>

    <section class="extras bg-accent-light">
      <h2>In the Wild</h2>
      <div 
        class="extra" 
        v-for="extra in extras" 
        v-if="!extra.hidden">
        <h4><a :href="extra.link" target="_blank">{{extra.title}}</a></h4>
        <p class="p_small">{{extra.description}}</p>
      </div>
    </section>

    <footer class="footer clearfix bg-accent">
      <div class="footer-section text-left">
        <span class="footer-credit">
          Powered by <a href="https://darksky.net/poweredby/" target="_blank">DarkSky</a>
        </span>
        <span class="footer-credit">
          View source on <a href="https://github.com/thalida" target="_blank">Github</a>
        </span>
      </div>
      <div class="footer-section text-right">
        <a href="https://twitter.com/thalidanoel" target="_blank">@thalidanoel</a>
      </div>
    </footer>
  </div>
  <!-- Project 1 -->
  <div class="root" v-else-if="whatwewant === 'project1'">
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
        <div style="z-index:1;left:0;right:0;opacity:1;position:relative;" v-on:click="onHomeClick()"><div class="LandingContainer__Background-s1msgrgs-1 goxDyi"><a class="LandingContainer__HomeLink-s1msgrgs-2 koaneT" href=""><div><div class="Icon__IconContainer-s1eymix-0 clAVox" role="img" aria-label="arrow-down icon"><canvas class="Icon__CanvasShim-s1eymix-1 hvTkVn" width="32" height="32"></canvas><svg class="Icon-s1eymix-2 kALlyJ" width="32" height="32" viewBox="0 0 32 32"><g fill-rule="evenodd"><path transform="rotate(-45 26.616 9.647)" d="M5.364 -0.236H7.364V15.764H5.364z"></path><path transform="scale(-1 1) rotate(-45 -1.419 53.188)" d="M5.364 9.764H7.364V25.764H5.364z"></path><path d="M2 14H26V16H2z" transform="rotate(-90 15 14)"></path></g></svg></div> Home</div></a></div></div>
    </div>
    <!-- Project 2 -->
</template>

<style scoped lang="scss">
  @import '../assets/styles/_variables';

  $padding-base: 32px;

  .p1 {
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    padding: 0;
    margin: 0;
  }

  section {
    margin: 0;
    padding: $padding-base;
    
    @media (min-width: $media-md) and (max-width: $media-lg) { 
      padding: $padding-base * 1.5;
    }
    
    @media (min-width: $media-lg) { 
      padding: $padding-base * 2;
    }
  }

  .bg-accent {
    background-color: rgb(16, 17, 49);
    color: #FFFFFF;
  }
  
  .bg-accent-light {
    background-color: #F9F7FE;
  }

  .photo {
    display: block;
    padding: 0;
    height: 280px;
    width: 100%;
    background-color: rgba(149,255,232,0.1);
    background-size: cover;
    background-repeat: no-repeat;

    &.etsy-photo {
      background-image: url(../assets/images/etsy-photo.png);
      background-position: center bottom;
    }

    &.reading-photo {
      background-image: url(../assets/images/reading-photo.jpg);
      background-position: center 60%;

      @media (min-width: 500px) { 
        background-position: center 50%;
      }
    }

    &.coding-photo {
      background-image: url(../assets/images/coding-photo.jpg);
      background-position: center center;
    }
  }

  .caption {
    padding: 4px 8px;

    background-color: rgba(0, 0, 0, 0.02);

    font-weight: 400;
    font-size: 10px;
    color: rgba($color-dark, 0.50);
    text-align: right;

    a {
      color: rgba($color-dark, 0.70);
    }
  }

  .project,
  .extra {
    padding-top: 16px;
    padding-bottom: 16px;

    &:last-child {
      padding-bottom: 0;
    }

    .project-links {
      margin-top: 8px;
      a {
        margin-right: 8px;
      }
    }
  }

  .featured-project,
  .about {
    p {
      padding-top: 16px;
    }
  }

  .work {
    .job {
      padding-top: 16px;
      padding-bottom: 16px;
    }

    .job-header {
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      padding: 0;
      margin: 0;
      
      font-weight: 400;
      font-size: 16px;
      line-height: 22px;
    }

    .job-company {
      flex: 0 1 auto;
    }

    .job-duration {
      display: none;
      flex: 0 1 auto; 
      text-align: right;
      font-weight: 300;
      font-size: 14px;
    }

    @media (min-width: $media-md) {
      .job-duration {
        display: block;
      }
    }
  }

  .footer {
    display: flex;
    align-items: center;
    padding: ($padding-base / 2);

    .footer-section {
      flex: 0 1 auto;
      width: 50%;
    }
    
    .footer-credit {
      display: block;
      text-transform: uppercase;
      font-size: 10px;
      padding: 4px 0;
    }
    
    @media (min-width: $media-md) and (max-width: $media-lg) { 
      padding-left: $padding-base * 1.5;
      padding-right: $padding-base * 1.5;
    }
    
    @media (min-width: $media-lg) { 
      padding-left: $padding-base * 2;
      padding-right: $padding-base * 2;
    }
  }

</style>
<style>
  @import '../assets/styles/style.css';
</style>