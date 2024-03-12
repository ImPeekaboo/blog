---
title: Testing
layout: video-google
SPDX-License-Identifier: LGPL-2.1-or-later
---

---

##  Testing

<div class="container">
  <video-js id="my-video" class="vjs-fluid vjs-layout-medium" controls preload="auto" poster="/assets/images/moona-cool.jpg">
    <source src="https://xx58j-my.sharepoint.com/:v:/g/personal/akunanime_xx58j_onmicrosoft_com/EcoOTGxEuRdNri9pCvsNc90BynBTW07P4GyMycxry4BWvw?download=1" type="video/mp4"/>
    <source src="https://teldrive.ayam.eu.org/api/files/adfo6gE5JzrStmqq/stream/pekolive-1080p60.mp4?hash=fd8aaf90b65f90e56214f69e264bd944" type="video/mp4"/>
  </video-js>
</div>
<script>
document.addEventListener('DOMContentLoaded', function() {
    var video = document.getElementById('my-video');
    var sources = video.getElementsByTagName('source');
    
    video.addEventListener('error', function() {
        // Iterate through all sources except the current one
        for (var i = 0; i < sources.length; i++) {
            if (sources[i].src !== video.src) {
                video.src = sources[i].src;
                video.load();
                break;
            }
        }
    });
});
</script>

---
