# WLC Config Begin <Wed Feb 26 09:50:00 2025>
! Number of APs: 9
! PID: AIR-AP1852I-E-K9,  SN: KWC213501ID 
! Product Version: 8.8.120.0 
! 
! ******************** PORT SUMMARY **********************
!  
!            STP   Admin   Physical   Physical   Link   Link
! Pr  Type   Stat   Mode     Mode      Status   Status  Trap     POE    
! -- ------- ---- ------- ---------- ---------- ------ ------- ---------
! 1  Normal  Forw Enable  Auto       1000 Full  Up     Enable  N/A     
! 
! ******************** CDP NEIGHBOUR SUMMARY **********************
! 
! Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
!                   S - Switch, H - Host, I - IGMP, r - Repeater, 
!                   M - Remotely Managed Device
! 
! Device ID        Local Intrfce     Holdtme    Capability  Platform  Port ID
! HOME_SW          wired0            147           R S I    WS-C2960X Gig 1/0/11

config location expiry tags 5 
config interface address management 10.0.10.200 255.255.255.0 10.0.10.254 
config interface dhcp service-port enable 
config interface address virtual 192.0.2.1 
config interface port management 1 
config flexconnect group default-flexgroup predownload enable 
config flexconnect group default-flexgroup vlan override-ap enable 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:60:98 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:64:60 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:64:e0 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:65:28 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:65:88 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:65:a8 
config flexconnect group default-flexgroup ap add a0:f8:49:e4:65:c0 
config flexconnect group default-flexgroup ap add a0:f8:49:e6:02:00 
config flexconnect group default-flexgroup ap add a0:f8:49:e6:03:50 
config flexconnect group default-flexgroup add 
config flexconnect group default-flexgroup radius ap authority info "Cisco A_ID" 
config flexconnect group default-flexgroup radius ap authority id 436973636f0000000000000000000000 
config flexconnect group default-flexgroup radius ap server-key encrypt 1 70e38c0219e2bce345eaecc34656ff8b 6bdd5dc069c9cb58750a8bd78b2a0684ae2e3864 82bd363766d731557160645815546e7f0c24a99387e2f7b821925ad3e4c31e 
config flexconnect group default-flexgroup avc 1 profile BuTtErFlY enable 
config flexconnect group default-flexgroup avc 2 profile Guests enable 
config flexconnect avc profile BuTtErFlY create 
config flexconnect avc profile BuTtErFlY apply 
config flexconnect avc profile Guests create 
config flexconnect avc profile Guests apply 
config ap mgmtuser add encrypt username Cisco password 1 2481c3905866d056814b7c041bada3a6 abf5755d09bed0b4e31cf051f94c1601c828b186 16 3457872f9832a6d071cfd8a9ff2e548a0000000000000000000000000000000000000000000000000000000000000000 24312434444e6f24673250775158506b384b52393859334c4568516c562f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000 secret encrypt 2431246e565269247543576833504131663747694f4f6c2e5a677168713000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000 all 
config ap preferred-mode ipv4 all 
config ap tcp-adjust-mss enable all 1250 
config ap antenna monitoring all detection-time 12 
config ap antenna monitoring all rssi-failure-threshold 40 
config ap antenna monitoring all weak-rssi 60 
config ap dtls-version dtls_all 
config ap packet-dump capture-time 10 
config ap packet-dump buffer-size 2048 
config ap packet-dump truncate 0 
config mdns profile create default-mdns-profile 
config mdns profile service add default-mdns-profile AirTunes 
config mdns profile service add default-mdns-profile Airplay 
config mdns profile service add default-mdns-profile Googlecast 
config mdns profile service add default-mdns-profile HP_Photosmart_Printer_1 
config mdns profile service add default-mdns-profile HP_Photosmart_Printer_2 
config mdns profile service add default-mdns-profile HomeSharing 
config mdns profile service add default-mdns-profile Printer-IPP 
config mdns profile service add default-mdns-profile Printer-IPPS 
config mdns profile service add default-mdns-profile Printer-LPD 
config mdns profile service add default-mdns-profile Printer-SOCKET 
config mdns profile service add default-mdns-profile iTuneWirelessDeviceSharing_2 
config mdns service create AirTunes _raop._tcp.local. origin all lss disable 
config mdns service origin all AirTunes 
config mdns service lss disable AirTunes 
config mdns service create Airplay _airplay._tcp.local. origin all lss disable 
config mdns service origin all Airplay 
config mdns service lss disable Airplay 
config mdns service create Googlecast _googlecast._tcp.local. origin all lss disable 
config mdns service origin all Googlecast 
config mdns service lss disable Googlecast 
config mdns service query enable HP_Photosmart_Printer_1 
config mdns service create HP_Photosmart_Printer_1 _universal._sub._ipp._tcp.local. origin all lss disable query enable 
config mdns service origin all HP_Photosmart_Printer_1 
config mdns service lss disable HP_Photosmart_Printer_1 
config mdns service query enable HP_Photosmart_Printer_2 
config mdns service create HP_Photosmart_Printer_2 _cups._sub._ipp._tcp.local. origin all lss disable query enable 
config mdns service origin all HP_Photosmart_Printer_2 
config mdns service lss disable HP_Photosmart_Printer_2 
config mdns service query enable HomeSharing 
config mdns service create HomeSharing _home-sharing._tcp.local. origin all lss disable query enable 
config mdns service origin all HomeSharing 
config mdns service lss disable HomeSharing 
config mdns service create Printer-IPP _ipp._tcp.local. origin all lss disable 
config mdns service origin all Printer-IPP 
config mdns service lss disable Printer-IPP 
config mdns service create Printer-IPPS _ipps._tcp.local. origin all lss disable 
config mdns service origin all Printer-IPPS 
config mdns service lss disable Printer-IPPS 
config mdns service create Printer-LPD _printer._tcp.local. origin all lss disable 
config mdns service origin all Printer-LPD 
config mdns service lss disable Printer-LPD 
config mdns service create Printer-SOCKET _pdl-datastream._tcp.local. origin all lss disable 
config mdns service origin all Printer-SOCKET 
config mdns service lss disable Printer-SOCKET 
config mdns service create iTuneWirelessDeviceSharing_2 _apple-mobdev2._tcp.local. origin all lss disable 
config mdns service origin all iTuneWirelessDeviceSharing_2 
config mdns service lss disable iTuneWirelessDeviceSharing_2 
config tacacs dns serverip 0.0.0.0 
config switchconfig strong-pwd position-check enable 
config switchconfig strong-pwd case-digit-check enable 
config switchconfig strong-pwd lockout attempts mgmtuser 3 
config switchconfig strong-pwd lockout time mgmtuser 5 
config policy schedule_policy_2 create 
config policy schedule_policy_2 wlan-schedule add enable hours 04:12 08:21 days mon 
config mesh convergence 
config sysname BuTtErFlY 
config time timezone location 16 
config time ntp interval 86400 
config time ntp server 1 0.ciscome.pool.ntp.org 
config time ntp server 2 1.ciscome.pool.ntp.org 
config time ntp server 3 2.ciscome.pool.ntp.org 
config 802.11b rate disabled 1 
config 802.11b rate disabled 2 
config 802.11b rate disabled 5.5 
config 802.11b rate disabled 11 
config 802.11b rate disabled 6 
config 802.11b rate mandatory 12 
config 802.11b 11gsupport enable 
config 802.11b cac voice sip codec g711 sample-interval 20 
config 802.11b cac voice sip bandwidth 64 sample-interval 20 
config 802.11b cleanair alarm device enable 802.11-nonstd 
config 802.11b cleanair alarm device enable 802.11-inv 
config 802.11b cleanair alarm device enable jammer 
config 802.11b cleanair enable network 
config advanced 802.11a channel add 36 
config advanced 802.11a channel add 40 
config advanced 802.11a channel add 44 
config advanced 802.11a channel add 48 
config advanced 802.11a channel add 52 
config advanced 802.11a channel add 56 
config advanced 802.11a channel add 60 
config advanced 802.11a channel add 64 
config advanced 802.11a channel add 100 
config advanced 802.11a channel add 104 
config advanced 802.11a channel add 108 
config advanced 802.11a channel add 112 
config advanced 802.11a channel add 116 
config advanced 802.11a channel add 120 
config advanced 802.11a channel add 124 
config advanced 802.11a channel add 128 
config advanced 802.11a channel add 132 
config advanced 802.11a channel add 136 
config advanced 802.11a channel add 140 
config advanced 802.11a channel dca chan-width best 
config advanced 802.11a channel pda-prop enable 
config advanced 802.11a packet bronze max-client-count 0 
config advanced 802.11a packet bronze max-retry 0 
config advanced 802.11a packet bronze timeout 0 
config advanced 802.11a packet bronze max-packet-count 0 
config advanced 802.11a packet silver max-client-count 0 
config advanced 802.11a packet silver max-retry 0 
config advanced 802.11a packet silver timeout 0 
config advanced 802.11a packet silver max-packet-count 0 
config advanced 802.11a packet gold max-client-count 0 
config advanced 802.11a packet gold max-retry 0 
config advanced 802.11a packet gold timeout 0 
config advanced 802.11a packet gold max-packet-count 0 
config advanced 802.11a packet platinum max-client-count 0 
config advanced 802.11a packet platinum max-retry 0 
config advanced 802.11a packet platinum timeout 0 
config advanced 802.11a packet platinum max-packet-count 0 
config advanced 802.11b channel add 1 
config advanced 802.11b channel add 6 
config advanced 802.11b channel add 11 
config advanced 802.11b channel pda-prop enable 
config advanced 802.11b channel cleanair-event sensitivity low 
config advanced 802.11b packet bronze max-client-count 0 
config advanced 802.11b packet bronze max-retry 0 
config advanced 802.11b packet bronze timeout 0 
config advanced 802.11b packet bronze max-packet-count 0 
config advanced 802.11b packet silver max-client-count 0 
config advanced 802.11b packet silver max-retry 0 
config advanced 802.11b packet silver timeout 0 
config advanced 802.11b packet silver max-packet-count 0 
config advanced 802.11b packet gold max-client-count 0 
config advanced 802.11b packet gold max-retry 0 
config advanced 802.11b packet gold timeout 0 
config advanced 802.11b packet gold max-packet-count 0 
config advanced 802.11b packet platinum max-client-count 0 
config advanced 802.11b packet platinum max-retry 0 
config advanced 802.11b packet platinum timeout 0 
config advanced 802.11b packet platinum max-packet-count 0 
config advanced probe limit 2 500 
config database size 2048 
config mgmtuser add encrypt Cisco 1 2cb8ae51bd584b5a4d1b84412ac12ad7 3bb42f266ef8ca7bfafa84deb993177dbb6bc8a9 16 78976983e469369a41eeb6e03351e92e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000 read-write 
config mgmtuser add encrypt_v1 Cisco 1 d542664cb9b88d7161219e7b447b5acc cff9be903d01e8ff3dc4ab59d2130638ad2ade46 16 1b7ce375f8901c9eb7370834821e929e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000 read-write 
config mgmtuser telnet Cisco enable 
config service samp-stats statistics-interval 120 
config network mgmt-via-wireless enable 
config network profile typical 
config network multicast l2mcast disable service-port 
config network multicast l2mcast disable virtual 
config network fast-ssid-change enable 
config network rf-network-name default 
config nmsp notification interval rssi rfid 2 
config countries-list add SA  
config country SA 
config radius callstationidtype ipaddr 
config radius dns serverip 0.0.0.0 
config remote-lan flexconnect local-switching 1 enable 
config remote-lan flexconnect local-switching 2 enable 
config wlan interface 1 management 
config wlan flexconnect local-switching 1 enable 
config wlan interface 2 management 
config wlan flexconnect local-switching 2 enable 
config wlan assisted-roaming neighbor-list enable 1 
config wlan assisted-roaming neighbor-list enable 2 
config wlan dhcp-scope 1 scope-name none 
config wlan mdns disable 1 
config wlan exclusionlist 1 180 
config wlan dhcp-scope 2 scope-name none 
config wlan mdns profile 2 none 
config wlan mdns disable 2 
config wlan exclusionlist 2 180 
config wlan bss-transition enable 1 
config wlan mfp client enable 1 
config wlan create 1 BuTtErFlY BuTtErFlY 
config wlan band-select allow enable 1 
config wlan policy add 1 schedule_policy_2 2 
config wlan bss-transition enable 2 
config wlan radius_server auth disable 2 
config wlan mfp client enable 2 
config wlan create 2 Guests Guests 
config wlan band-select allow enable 2 
config wlan broadcast-ssid enable 1 
config wlan broadcast-ssid disable 2 
config wlan ccx aironetiesupport disable 1 
config wlan ccx aironetiesupport disable 2 
config wlan hotspot dot11u ipaddr-type 0 0 2 
config wlan hotspot dot11u auth-type 0 2 
config wlan hotspot dot11u network-type 2 0 0 
config wlan dms enable 1 
config wlan session-timeout 1 0 
config wlan wmm allow 1 
config wlan dms enable 2 
config wlan session-timeout 2 0 
config wlan wmm allow 2 
config wlan security web-auth server-precedence 1 local radius ldap 
config wlan security wpa akm 802.1x disable 1 
config wlan security wpa akm psk set-key hex encrypt 1 2ee61ea676b9612a4151532f3b48c54a 5072323028e03719d250835eede7e54bdfc238ac 48 c632b57d6b071623cf97807d65ad9a565cb32dd7e252ba9a86c82fb7ddfd69c409757d3e009e81147c88199d58f6538b0000000000000000c40ed12ab00e3c347cd39c2d48e5ad2a1f030000a0d39c2d00d79c2d34148a40000000000a000000b4193c340000000000000000cce7082f48e5ad2a64148a409425d12ab4193c34c4d39c2dffffffff8000000048a1ea2f 1 
config wlan security wpa akm psk enable 1 
config wlan security wpa enable 1 
config wlan security ft adaptive enable 1 
config wlan enable 1 
config wlan security web-auth captive-bypass enable 2 
config wlan security web-auth server-precedence 2 local radius ldap 
config wlan security web-passthrough email-input enable 2 
config wlan security web-passthrough enable 2 
config wlan security wpa akm 802.1x disable 2 
config wlan security wpa wpa2 ciphers aes disable 2 
config wlan security wpa wpa2 disable 2 
config wlan security wpa disable 2 
config wlan security ft adaptive enable 2 
config rogue client mse enable 
config rogue ap rldp enable alarm-only monitor-ap-only 
config rogue detection transient-rogue-interval 300 
config rogue detection monitor-ap transient-rogue-interval 300 
config rogue detection monitor-ap report-interval 30 
config rogue detection min-rssi -80 
config rogue detection report-interval 30 
config rogue detection security-level high 
config rogue auto-contain level 0 
config rogue containment auto-rate enable 
config 802.11a rate disabled 6 
config 802.11a rate disabled 9 
config 802.11a cac voice sip codec g711 sample-interval 20 
config 802.11a cac voice sip bandwidth 64 sample-interval 20 
config 802.11a cleanair alarm device enable 802.11-nonstd 
config 802.11a cleanair alarm device enable jammer 
config 802.11a cleanair alarm device enable 802.11-inv 
config 802.11a cleanair enable network 
config dhcp proxy disable bootp-broadcast disable 
config rf-profile channel add 36 High-Client-Density-802.11a 
config rf-profile channel add 40 High-Client-Density-802.11a 
config rf-profile channel add 44 High-Client-Density-802.11a 
config rf-profile channel add 48 High-Client-Density-802.11a 
config rf-profile channel add 52 High-Client-Density-802.11a 
config rf-profile channel add 56 High-Client-Density-802.11a 
config rf-profile channel add 60 High-Client-Density-802.11a 
config rf-profile channel add 64 High-Client-Density-802.11a 
config rf-profile channel add 149 High-Client-Density-802.11a 
config rf-profile channel add 153 High-Client-Density-802.11a 
config rf-profile channel add 157 High-Client-Density-802.11a 
config rf-profile channel add 161 High-Client-Density-802.11a 
config rf-profile channel add 100 High-Client-Density-802.11a 
config rf-profile channel add 104 High-Client-Density-802.11a 
config rf-profile channel add 108 High-Client-Density-802.11a 
config rf-profile channel add 112 High-Client-Density-802.11a 
config rf-profile channel add 116 High-Client-Density-802.11a 
config rf-profile channel add 120 High-Client-Density-802.11a 
config rf-profile channel add 124 High-Client-Density-802.11a 
config rf-profile channel add 128 High-Client-Density-802.11a 
config rf-profile channel add 132 High-Client-Density-802.11a 
config rf-profile channel add 136 High-Client-Density-802.11a 
config rf-profile channel add 140 High-Client-Density-802.11a 
config rf-profile channel chan-width 20 High-Client-Density-802.11a 
config rf-profile create 802.11a High-Client-Density-802.11a 
config rf-profile tx-power-min 7 High-Client-Density-802.11a 
config rf-profile channel add 1 High-Client-Density-802.11bg 
config rf-profile channel add 6 High-Client-Density-802.11bg 
config rf-profile channel add 11 High-Client-Density-802.11bg 
config rf-profile channel chan-width 20 High-Client-Density-802.11bg 
config rf-profile create 802.11b High-Client-Density-802.11bg 
config rf-profile tx-power-min 7 High-Client-Density-802.11bg 
config rf-profile channel add 36 Low-Client-Density-802.11a 
config rf-profile channel add 40 Low-Client-Density-802.11a 
config rf-profile channel add 44 Low-Client-Density-802.11a 
config rf-profile channel add 48 Low-Client-Density-802.11a 
config rf-profile channel add 52 Low-Client-Density-802.11a 
config rf-profile channel add 56 Low-Client-Density-802.11a 
config rf-profile channel add 60 Low-Client-Density-802.11a 
config rf-profile channel add 64 Low-Client-Density-802.11a 
config rf-profile channel add 149 Low-Client-Density-802.11a 
config rf-profile channel add 153 Low-Client-Density-802.11a 
config rf-profile channel add 157 Low-Client-Density-802.11a 
config rf-profile channel add 161 Low-Client-Density-802.11a 
config rf-profile channel add 100 Low-Client-Density-802.11a 
config rf-profile channel add 104 Low-Client-Density-802.11a 
config rf-profile channel add 108 Low-Client-Density-802.11a 
config rf-profile channel add 112 Low-Client-Density-802.11a 
config rf-profile channel add 116 Low-Client-Density-802.11a 
config rf-profile channel add 120 Low-Client-Density-802.11a 
config rf-profile channel add 124 Low-Client-Density-802.11a 
config rf-profile channel add 128 Low-Client-Density-802.11a 
config rf-profile channel add 132 Low-Client-Density-802.11a 
config rf-profile channel add 136 Low-Client-Density-802.11a 
config rf-profile channel add 140 Low-Client-Density-802.11a 
config rf-profile channel chan-width 20 Low-Client-Density-802.11a 
config rf-profile coverage level 2 Low-Client-Density-802.11a 
config rf-profile coverage voice -90 Low-Client-Density-802.11a 
config rf-profile coverage data -90 Low-Client-Density-802.11a 
config rf-profile create 802.11a Low-Client-Density-802.11a 
config rf-profile channel add 1 Low-Client-Density-802.11bg 
config rf-profile channel add 6 Low-Client-Density-802.11bg 
config rf-profile channel add 11 Low-Client-Density-802.11bg 
config rf-profile channel chan-width 20 Low-Client-Density-802.11bg 
config rf-profile coverage level 2 Low-Client-Density-802.11bg 
config rf-profile coverage voice -90 Low-Client-Density-802.11bg 
config rf-profile coverage data -90 Low-Client-Density-802.11bg 
config rf-profile create 802.11b Low-Client-Density-802.11bg 
config rf-profile channel add 36 Typical-Client-Density-802.11a 
config rf-profile channel add 40 Typical-Client-Density-802.11a 
config rf-profile channel add 44 Typical-Client-Density-802.11a 
config rf-profile channel add 48 Typical-Client-Density-802.11a 
config rf-profile channel add 52 Typical-Client-Density-802.11a 
config rf-profile channel add 56 Typical-Client-Density-802.11a 
config rf-profile channel add 60 Typical-Client-Density-802.11a 
config rf-profile channel add 64 Typical-Client-Density-802.11a 
config rf-profile channel add 149 Typical-Client-Density-802.11a 
config rf-profile channel add 153 Typical-Client-Density-802.11a 
config rf-profile channel add 157 Typical-Client-Density-802.11a 
config rf-profile channel add 161 Typical-Client-Density-802.11a 
config rf-profile channel add 100 Typical-Client-Density-802.11a 
config rf-profile channel add 104 Typical-Client-Density-802.11a 
config rf-profile channel add 108 Typical-Client-Density-802.11a 
config rf-profile channel add 112 Typical-Client-Density-802.11a 
config rf-profile channel add 116 Typical-Client-Density-802.11a 
config rf-profile channel add 120 Typical-Client-Density-802.11a 
config rf-profile channel add 124 Typical-Client-Density-802.11a 
config rf-profile channel add 128 Typical-Client-Density-802.11a 
config rf-profile channel add 132 Typical-Client-Density-802.11a 
config rf-profile channel add 136 Typical-Client-Density-802.11a 
config rf-profile channel add 140 Typical-Client-Density-802.11a 
config rf-profile channel chan-width 20 Typical-Client-Density-802.11a 
config rf-profile create 802.11a Typical-Client-Density-802.11a 
config rf-profile channel add 1 Typical-Client-Density-802.11bg 
config rf-profile channel add 6 Typical-Client-Density-802.11bg 
config rf-profile channel add 11 Typical-Client-Density-802.11bg 
config rf-profile channel chan-width 20 Typical-Client-Density-802.11bg 
config rf-profile create 802.11b Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11a disabled 6 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a disabled 9 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a mandatory 12 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 18 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a mandatory 24 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 36 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 48 High-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 54 High-Client-Density-802.11a 
config rf-profile tx-power-control-thresh-v1 -65 High-Client-Density-802.11a 
config rf-profile rx-sop threshold -78 High-Client-Density-802.11a 
config rf-profile data-rates 802.11b disabled 1 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 2 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 5.5 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 11 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 6 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 9 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b mandatory 12 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 18 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 24 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 36 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 48 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 54 High-Client-Density-802.11bg 
config rf-profile rx-sop threshold -82 High-Client-Density-802.11bg 
config rf-profile data-rates 802.11a mandatory 6 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 9 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a mandatory 12 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 18 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a mandatory 24 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 36 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 48 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 54 Low-Client-Density-802.11a 
config rf-profile tx-power-control-thresh-v1 -60 Low-Client-Density-802.11a 
config rf-profile rx-sop threshold -80 Low-Client-Density-802.11a 
config rf-profile data-rates 802.11b mandatory 1 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b mandatory 2 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b mandatory 5.5 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b mandatory 11 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 6 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 9 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 12 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 18 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 24 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 36 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 48 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 54 Low-Client-Density-802.11bg 
config rf-profile tx-power-control-thresh-v1 -65 Low-Client-Density-802.11bg 
config rf-profile rx-sop threshold -85 Low-Client-Density-802.11bg 
config rf-profile data-rates 802.11a mandatory 6 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 9 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a mandatory 12 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 18 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a mandatory 24 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 36 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 48 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11a supported 54 Typical-Client-Density-802.11a 
config rf-profile data-rates 802.11b disabled 1 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 2 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 5.5 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 11 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b disabled 6 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 9 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b mandatory 12 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 18 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 24 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 36 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 48 Typical-Client-Density-802.11bg 
config rf-profile data-rates 802.11b supported 54 Typical-Client-Density-802.11bg 
config rfid status enable 
config rfid timeout 1200 
config rfid rate-limit 1000 
config rfid mobility pango disable 
config qos priority platinum voice voice besteffort 
config qos dot1p-tag platinum 0 
config qos protocol-type platinum none 
config netuser maxuserlogin 5 
config snmp v3user delete default 
config macfilter add 2c:61:f6:80:9b:1b 0 0 Ipad 
config macfilter add f8:c3:9e:be:d5:b1 0 0 dady 
config macfilter add b0:68:e6:7e:3a:c9 0 0 "GF HALL" 
config macfilter add 1e:be:79:14:30:d0 0 0 x 
config macfilter add 44:e4:ee:88:c6:ee 0 0 MQL6 
config macfilter add 44:e4:ee:64:52:e2 0 0 Diwania 
config macfilter add 48:7e:48:55:65:f0 0 0 xiomi 
config macfilter add d2:46:7d:11:d9:71 0 0 cloud 
config macfilter add 58:91:cf:92:ff:36 0 0 "Aboud PC" 
config macfilter add ec:fa:5c:ec:d4:31 0 0 Mibox 
config macfilter add ac:89:95:af:ea:3d 0 0 th 
config macfilter add fe:bd:6f:86:64:5d 0 0 Lyan12 
transfer download ap-images cco-username $username 
transfer download ap-images cco-auto-check disable 
transfer download ap-images mode cco 
transfer download ap-images cco-password $password 

# WLC Config End <Wed Feb 26 09:50:02 2025>
