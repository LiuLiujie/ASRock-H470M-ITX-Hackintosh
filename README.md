# ASRock-H470M-ITX-Hackintosh

ASRock H470M-ITX/AC Hacintosh with opencore 0.7.5, working at macOS Monterey 12.0.1

## Newest Update(2021-11-10)
The FakePCIID.kext will cause KP in macOS Monterey, so I change the FV-T919 wireless card to an AMD dGP, which means that the people only use iGPU should not use the EFI for Monterey. 
Also, there might be a workaround for iGPU only user to use Monterey. The FakePCIID.kext and FakePCIID_Intel_HDMI_Audio.kext are used to make the speaker on the minitor work. If you have no speaker on the monitor, you can try removing these two kext. But I didn't test this solution.

## Device list
| Device          | Type                                                         | Infomation                                                   |
| --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| CPU             | i9-10900                                                      | normal frequency shift                                       |
| iGPU            | UHD630                                                       | 4K decode normal，framebuffer injected，HEVC normal, on-board HDMI output |
| dPU            | RX560d                                             | AMD dGPU|
| Audio           | ACL1200                                                      | layout-id：49，injected，3.5 on the case normal, others no test |
| NetWork1         | Intel I217v                                                       | normal                                                       |
| NetWork2         | RTL8125BG                                                       | normal                                                       |
| Wifi&Bluetooth  | AX200                                                      | Intel wireless card can use itlwm                                  |
| USB             | 2\*USB2.0 and 6\*USB3.0 on board，<br />1\*USB2.0 and 1\*USB3.0 on case | customlized by kext                                          |
| Serial/UUDI/MLB | NOT GENERTATED                                                    | gen yours please                       |
