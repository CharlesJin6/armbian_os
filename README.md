<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts after **repository update** is done succesfully.
- Nightly images are build once per day, at 5:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a href=""><b>Board name</b></a></td><td align="left"><b>Started</b></td><td align=right><b>Kernel version</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td></tr><tr><td align="left"><a href="https://paste.armbian.com/ejimetasat">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;02:33:33</td><td align=right>6.1.46-current-sunxi64</td><td align=right>708</td><td align=right>2918</td></tr><tr><td align="left"><a href="https://paste.armbian.com/upitawirec">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;02:46:44</td><td align=right>5.15.93-sunxi64</td><td align=right>486</td><td align=right>2571</td></tr><tr><td align="left"><a href="https://paste.armbian.com/pasidigiba">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;02:59:32</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>881</td><td align=right>2862</td></tr><tr><td align="left"><a href="https://paste.armbian.com/mayefefaha">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;03:14:18</td><td align=right>6.1.11-sunxi64</td><td align=right>548</td><td align=right>2885</td></tr><tr><td align="left"><a href="https://paste.armbian.com/popabajeto">Espressobin</a></td><td align="left">2023-08-22&nbsp;02:40:38</td><td align=right>5.15.127-current-mvebu64</td><td align=right>864</td><td align=right>1026</td></tr><tr><td align="left"><a href="https://paste.armbian.com/aqekupovus">Espressobin</a></td><td align="left">2023-08-22&nbsp;03:04:05</td><td align=right>5.15.93-mvebu64</td><td align=right>730</td><td align=right>1004</td></tr><tr><td align="left"><a href="https://paste.armbian.com/atosenodix">Pine H64</a></td><td align="left">2023-08-22&nbsp;02:30:21</td><td align=right>6.1.46-current-sunxi64</td><td align=right>876</td><td align=right>3787</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zavazefoma">Pine H64</a></td><td align="left">2023-08-22&nbsp;02:40:38</td><td align=right>5.15.93-sunxi64</td><td align=right>801</td><td align=right>3688</td></tr><tr><td align="left"><a href="https://paste.armbian.com/avivihunal">Pine H64</a></td><td align="left">2023-08-22&nbsp;02:50:20</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>867</td><td align=right>3624</td></tr><tr><td align="left"><a href="https://paste.armbian.com/izequtijuf">Pine H64</a></td><td align="left">2023-08-22&nbsp;03:02:04</td><td align=right>6.1.11-sunxi64</td><td align=right>824</td><td align=right>3605</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;02:21:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;02:21:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;02:21:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;02:21:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;02:21:46</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;02:21:47</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/enunudekud">RockPro 64</a></td><td align="left">2023-08-22&nbsp;02:28:18</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6476</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ufoqokoguc">RockPro 64</a></td><td align="left">2023-08-22&nbsp;02:35:20</td><td align=right>5.15.93-rockchip64</td><td align=right>889</td><td align=right>6351</td></tr><tr><td align="left"><a href="https://paste.armbian.com/divuqaciku">RockPro 64</a></td><td align="left">2023-08-22&nbsp;02:42:05</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>865</td><td align=right>6484</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oqebinuxot">RockPro 64</a></td><td align="left">2023-08-22&nbsp;02:49:05</td><td align=right>6.1.11-rockchip64</td><td align=right>882</td><td align=right>6430</td></tr><tr><td align="left"><a href="https://paste.armbian.com/hojofaxado">Rockpi E</a></td><td align="left">2023-08-22&nbsp;02:36:47</td><td align=right>6.1.46-current-rockchip64</td><td align=right>90</td><td align=right>3347</td></tr><tr><td align="left"><a href="https://paste.armbian.com/opekidehak">Rockpi E</a></td><td align="left">2023-08-22&nbsp;02:50:02</td><td align=right>5.15.93-rockchip64</td><td align=right>90</td><td align=right>2881</td></tr><tr><td align="left"><a href="https://paste.armbian.com/viduzujaha">Rockpi E</a></td><td align="left">2023-08-22&nbsp;03:04:01</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>89</td><td align=right>3324</td></tr><tr><td align="left"><a href="https://paste.armbian.com/osufojaqem">Rockpi E</a></td><td align="left">2023-08-22&nbsp;03:17:39</td><td align=right>6.1.11-rockchip64</td><td align=right>90</td><td align=right>2885</td></tr><tr><td align="left"><a href="https://paste.armbian.com/gituhitecu">Odroid C2</a></td><td align="left">2023-08-22&nbsp;02:31:16</td><td align=right>6.1.46-current-meson64</td><td align=right>881</td><td align=right>3953</td></tr><tr><td align="left"><a href="https://paste.armbian.com/kuxazoveru">Odroid C2</a></td><td align="left">2023-08-22&nbsp;02:42:38</td><td align=right>6.1.11-meson64</td><td align=right>860</td><td align=right>4058</td></tr><tr><td align="left"><a href="https://paste.armbian.com/dufuyisude">Odroid C2</a></td><td align="left">2023-08-22&nbsp;02:54:24</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>4026</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xejivitifu">Odroid C2</a></td><td align="left">2023-08-22&nbsp;03:06:37</td><td align=right>6.2.0-rc3-meson64</td><td align=right>829</td><td align=right>4028</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jukuzagumu">NanoPi R6S</a></td><td align="left">2023-08-22&nbsp;02:24:59</td><td align=right>5.10.160-legacy-rk35xx</td><td align=right>2370</td><td align=right>15734</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vinuholero">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;02:30:26</td><td align=right>6.1.46-current-sunxi64</td><td align=right>877</td><td align=right>3913</td></tr><tr><td align="left"><a href="https://paste.armbian.com/tuwojexayu">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;02:40:29</td><td align=right>5.15.93-sunxi64</td><td align=right>866</td><td align=right>3839</td></tr><tr><td align="left"><a href="https://paste.armbian.com/rapenolidu">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;02:50:05</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>875</td><td align=right>3833</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ecigecekux">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;03:00:31</td><td align=right>6.1.11-sunxi64</td><td align=right>871</td><td align=right>3887</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oxuqalohek">Odroid C4</a></td><td align="left">2023-08-22&nbsp;02:29:00</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>5646</td></tr><tr><td align="left"><a href="https://paste.armbian.com/elovucarux">Odroid C4</a></td><td align="left">2023-08-22&nbsp;02:37:38</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>5599</td></tr><tr><td align="left"><a href="https://paste.armbian.com/gugugizibe">Odroid C4</a></td><td align="left">2023-08-22&nbsp;02:45:39</td><td align=right>6.4.11-edge-meson64</td><td align=right>880</td><td align=right>5541</td></tr><tr><td align="left"><a href="https://paste.armbian.com/atejigapob">Odroid C4</a></td><td align="left">2023-08-22&nbsp;02:55:12</td><td align=right>6.2.0-rc3-meson64</td><td align=right>890</td><td align=right>5617</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oyozomofez">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;02:29:02</td><td align=right>6.1.46-current-rockchip64</td><td align=right>860</td><td align=right>6440</td></tr><tr><td align="left"><a href="https://paste.armbian.com/pibajitape">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;02:36:24</td><td align=right>5.15.93-rockchip64</td><td align=right>881</td><td align=right>6311</td></tr><tr><td align="left"><a href="https://paste.armbian.com/evicesuvam">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;02:43:46</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>830</td><td align=right>6320</td></tr><tr><td align="left"><a href="https://paste.armbian.com/fabavibore">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;02:51:18</td><td align=right>6.1.11-rockchip64</td><td align=right>890</td><td align=right>6320</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qopanidavo">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;02:28:41</td><td align=right>6.1.46-current-rockchip64</td><td align=right>960</td><td align=right>6708</td></tr><tr><td align="left"><a href="https://paste.armbian.com/asahecovoc">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;02:36:12</td><td align=right>5.15.93-rockchip64</td><td align=right>960</td><td align=right>6598</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uzijabopoh">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;02:43:13</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>751</td><td align=right>6760</td></tr><tr><td align="left"><a href="https://paste.armbian.com/olekilucuk">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;02:50:11</td><td align=right>6.1.11-rockchip64</td><td align=right>898</td><td align=right>6663</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iwulozeneq">Banana Pi Pro</a></td><td align="left">2023-08-22&nbsp;02:35:38</td><td align=right>6.1.46-current-sunxi</td><td align=right>512</td><td align=right>1014</td></tr><tr><td align="left"><a href="https://paste.armbian.com/agexocotog">Banana Pi Pro</a></td><td align="left">2023-08-22&nbsp;02:51:06</td><td align=right>5.15.93-sunxi</td><td align=right>381</td><td align=right>1031</td></tr><tr><td align="left"><a href="https://paste.armbian.com/idogokegij">Banana Pi Pro</a></td><td align="left">2023-08-22&nbsp;03:05:42</td><td align=right>6.4.11-edge-sunxi</td><td align=right>316</td><td align=right>1017</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eyewiwaraz">ZeroPi</a></td><td align="left">2023-08-22&nbsp;02:31:39</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>551</td><td align=right>2627</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xivecupuje">ZeroPi</a></td><td align="left">2023-08-22&nbsp;02:39:32</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>533</td><td align=right>2636</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ritepigoro">ZeroPi</a></td><td align="left">2023-08-22&nbsp;02:46:53</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>554</td><td align=right>2653</td></tr><tr><td align="left"><a href="https://paste.armbian.com/fixonefofo">ZeroPi</a></td><td align="left">2023-08-22&nbsp;02:54:58</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>540</td><td align=right>2650</td></tr><tr><td align="left"><a href="https://paste.armbian.com/kivotuhume">ZeroPi</a></td><td align="left">2023-08-22&nbsp;03:04:29</td><td align=right>6.4.11-edge-sunxi</td><td align=right>557</td><td align=right>2658</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wuqatokuno">ZeroPi</a></td><td align="left">2023-08-22&nbsp;03:12:45</td><td align=right>6.4.11-edge-sunxi</td><td align=right>560</td><td align=right>2644</td></tr><tr><td align="left"><a href="https://paste.armbian.com/tixihixage">Cubietruck</a></td><td align="left">2023-08-22&nbsp;02:39:03</td><td align=right>6.1.46-current-sunxi</td><td align=right>431</td><td align=right>995</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bikosiriwi">Cubietruck</a></td><td align="left">2023-08-22&nbsp;03:01:46</td><td align=right>5.15.93-sunxi</td><td align=right>463</td><td align=right>989</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xazazorawe">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;02:28:44</td><td align=right>6.1.46-current-rockchip64</td><td align=right>950</td><td align=right>6489</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wipulajitu">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;02:37:07</td><td align=right>5.15.93-rockchip64</td><td align=right>960</td><td align=right>6451</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lafuyisaba">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;02:44:50</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>880</td><td align=right>6405</td></tr><tr><td align="left"><a href="https://paste.armbian.com/udamesigoh">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;02:53:54</td><td align=right>6.1.11-rockchip64</td><td align=right>900</td><td align=right>6510</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xulikuyigi">Odroid N2</a></td><td align="left">2023-08-22&nbsp;02:26:00</td><td align=right>6.1.46-current-meson64</td><td align=right>880</td><td align=right>8847</td></tr><tr><td align="left"><a href="https://paste.armbian.com/udocobizik">Odroid N2</a></td><td align="left">2023-08-22&nbsp;02:31:31</td><td align=right>6.1.11-meson64</td><td align=right>870</td><td align=right>8644</td></tr><tr><td align="left"><a href="https://paste.armbian.com/holusacave">Odroid N2</a></td><td align="left">2023-08-22&nbsp;02:36:49</td><td align=right>6.4.11-edge-meson64</td><td align=right>896</td><td align=right>8923</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wiyanipuqi">Odroid N2</a></td><td align="left">2023-08-22&nbsp;02:42:20</td><td align=right>6.2.0-rc3-meson64</td><td align=right>810</td><td align=right>8792</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;02:21:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;02:21:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;02:21:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;02:21:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/izujasijiz">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;02:29:34</td><td align=right>6.1.46-current-rockchip64</td><td align=right>828</td><td align=right>3446</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lozexopozi">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;02:39:33</td><td align=right>5.15.93-rockchip64</td><td align=right>888</td><td align=right>2552</td></tr><tr><td align="left"><a href="https://paste.armbian.com/dutokoxava">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;02:49:46</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>791</td><td align=right>2018</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iridukagoz">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;03:01:14</td><td align=right>6.1.11-rockchip64</td><td align=right>767</td><td align=right>1887</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;02:21:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;02:21:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;02:21:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;02:21:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;02:21:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;02:21:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ifagukojel">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;02:34:18</td><td align=right>6.1.46-current-sunxi64</td><td align=right>773</td><td align=right>2478</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uzufikurab">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;02:48:45</td><td align=right>5.15.93-sunxi64</td><td align=right>813</td><td align=right>2441</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ebakaleqon">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;03:05:10</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>839</td><td align=right>2523</td></tr><tr><td align="left"><a href="https://paste.armbian.com/tohogakano">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;03:19:48</td><td align=right>6.1.11-sunxi64</td><td align=right>708</td><td align=right>2464</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ebohirefoq">Orange Pi Zero2</a></td><td align="left">2023-08-22&nbsp;02:33:09</td><td align=right>6.1.46-current-sunxi64</td><td align=right>779</td><td align=right>2832</td></tr><tr><td align="left"><a href="https://paste.armbian.com/kosoziqenu">Orange Pi Zero2</a></td><td align="left">2023-08-22&nbsp;02:50:42</td><td align=right>5.15.93-sunxi64</td><td align=right>685</td><td align=right>1173</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;02:28:49</td><td align=right>6.1.46-current-mvebu</td><td align=right>878</td><td align=right>2224</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;02:37:25</td><td align=right>5.15.93-mvebu</td><td align=right>881</td><td align=right>2177</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;02:45:22</td><td align=right>6.2.16-edge-mvebu</td><td align=right>870</td><td align=right>2181</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;02:57:42</td><td align=right>6.1.11-mvebu</td><td align=right>901</td><td align=right>2175</td></tr><tr><td align="left"><a href="https://paste.armbian.com/efajicadis">ODROID M1</a></td><td align="left">2023-08-22&nbsp;02:31:25</td><td align=right>6.3.13-edge-rk3568-odroid</td><td align=right>889</td><td align=right>5246</td></tr><tr><td align="left"><a href="https://paste.armbian.com/guhakejire">ODROID M1</a></td><td align="left">2023-08-22&nbsp;02:41:57</td><td align=right>6.1.12-rk3568-odroid</td><td align=right>820</td><td align=right>5107</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zajopavopa">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;02:29:04</td><td align=right>6.1.46-current-rockchip64</td><td align=right>888</td><td align=right>6872</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zigehalaze">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;02:36:55</td><td align=right>5.15.93-rockchip64</td><td align=right>889</td><td align=right>6773</td></tr><tr><td align="left"><a href="https://paste.armbian.com/aloxusukoc">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;02:44:21</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>880</td><td align=right>6776</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vebufuticu">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;02:52:54</td><td align=right>6.1.11-rockchip64</td><td align=right>735</td><td align=right>6706</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bevejomori">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;02:29:31</td><td align=right>6.1.46-current-rockchip64</td><td align=right>961</td><td align=right>5599</td></tr><tr><td align="left"><a href="https://paste.armbian.com/odacibeqij">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;02:38:49</td><td align=right>5.15.93-rockchip64</td><td align=right>896</td><td align=right>4515</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vuliyorawi">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;02:46:49</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>960</td><td align=right>4809</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zeroqokoci">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;02:57:34</td><td align=right>6.1.11-rockchip64</td><td align=right>820</td><td align=right>4205</td></tr><tr><td align="left"><a href="https://paste.armbian.com/noderajaha">Le potato</a></td><td align="left">2023-08-22&nbsp;02:34:54</td><td align=right>6.1.46-current-meson64</td><td align=right>93</td><td align=right>3700</td></tr><tr><td align="left"><a href="https://paste.armbian.com/usakesowev">Le potato</a></td><td align="left">2023-08-22&nbsp;02:48:18</td><td align=right>6.1.11-meson64</td><td align=right>89</td><td align=right>3685</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ixabanejon">Le potato</a></td><td align="left">2023-08-22&nbsp;03:03:41</td><td align=right>6.4.11-edge-meson64</td><td align=right>90</td><td align=right>3724</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ehudihunek">Le potato</a></td><td align="left">2023-08-22&nbsp;03:17:37</td><td align=right>6.2.0-rc3-meson64</td><td align=right>93</td><td align=right>3697</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-22&nbsp;02:21:01</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-22&nbsp;02:21:02</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;02:21:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;02:21:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;02:21:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;02:21:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/tatujojuwe">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;02:26:47</td><td align=right>6.1.46-current-meson64</td><td align=right>880</td><td align=right>5569</td></tr><tr><td align="left"><a href="https://paste.armbian.com/epeteruzot">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;02:33:01</td><td align=right>6.1.11-meson64</td><td align=right>880</td><td align=right>5588</td></tr><tr><td align="left"><a href="https://paste.armbian.com/udepohugar">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;02:39:03</td><td align=right>6.4.11-edge-meson64</td><td align=right>870</td><td align=right>5557</td></tr><tr><td align="left"><a href="https://paste.armbian.com/udebecutip">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;02:45:16</td><td align=right>6.2.0-rc3-meson64</td><td align=right>880</td><td align=right>5550</td></tr><tr><td align="left"><a href="https://paste.armbian.com/gibixawona">Tinker Board</a></td><td align="left">2023-08-22&nbsp;02:28:20</td><td align=right>6.1.46-current-rockchip</td><td align=right>90</td><td align=right>5131</td></tr><tr><td align="left"><a href="https://paste.armbian.com/umuwuwokiw">Tinker Board</a></td><td align="left">2023-08-22&nbsp;02:35:23</td><td align=right>6.1.11-rockchip</td><td align=right>889</td><td align=right>4733</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qajoxoqofa">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;02:31:35</td><td align=right>6.1.46-current-meson64</td><td align=right>883</td><td align=right>6110</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oxavocopuh">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;02:43:06</td><td align=right>6.1.11-meson64</td><td align=right>851</td><td align=right>6151</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jibunodedi">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;02:54:02</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>6145</td></tr><tr><td align="left"><a href="https://paste.armbian.com/okovezajim">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;03:05:21</td><td align=right>6.2.0-rc3-meson64</td><td align=right>920</td><td align=right>6095</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lukalumewo">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;02:30:19</td><td align=right>6.1.46-current-meson64</td><td align=right>94</td><td align=right>3679</td></tr><tr><td align="left"><a href="https://paste.armbian.com/obasomokig">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;02:40:20</td><td align=right>6.1.11-meson64</td><td align=right>98</td><td align=right>3705</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oxafigeced">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;02:49:49</td><td align=right>6.4.11-edge-meson64</td><td align=right>90</td><td align=right>3677</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ijayepujom">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;02:59:50</td><td align=right>6.2.0-rc3-meson64</td><td align=right>88</td><td align=right>3694</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;02:20:50</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;02:20:51</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;02:20:52</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;02:20:53</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-22&nbsp;02:21:24</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-22&nbsp;02:21:24</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;02:21:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;02:21:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;02:21:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;02:21:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
