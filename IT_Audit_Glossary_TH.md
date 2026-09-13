# คลังคำศัพท์สำหรับการตรวจสอบ IT

หน้านี้รวบรวมคำที่มักได้ยินระหว่างการตรวจ IT โดยอธิบายแบบผู้เริ่มต้นและบอกว่าเหตุใดผู้ตรวจจึงสนใจ คำจำกัดความถูกย่อเพื่อใช้เรียนและสนทนากับผู้รับตรวจ รายละเอียดทางเทคนิคอาจแตกต่างตามผลิตภัณฑ์และสถาปัตยกรรมขององค์กร

วิธีอ่านที่แนะนำ: อย่าจำคำศัพท์แยกจากกัน ให้ถามเสมอว่า **สิ่งนี้คืออะไร → อยู่ตรงไหนในกระบวนการ → ใครรับผิดชอบ → เสี่ยงอะไร → มี Control และหลักฐานอะไร**

## 1. ระบบ เครือข่าย และการเชื่อมต่อ

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Network** | กลุ่มอุปกรณ์ที่เชื่อมต่อกันเพื่อสื่อสารและแลกเปลี่ยนข้อมูล | มีแผนผัง ผู้รับผิดชอบ การแบ่งเขต และ Monitoring ครบหรือไม่ |
| **Internet** | เครือข่ายสาธารณะทั่วโลกที่เชื่อมระบบจำนวนมากเข้าด้วยกัน | ระบบใดเปิดให้อินเทอร์เน็ตเข้าถึง ข้อมูลออกไปที่ใด และป้องกันภัยจากภายนอกอย่างไร |
| **Intranet** | เครือข่ายหรือเว็บไซต์ภายในองค์กรสำหรับพนักงาน | ผู้ใช้นอกองค์กรเข้าถึงได้หรือไม่ สิทธิ์และข้อมูลภายในเหมาะสมหรือไม่ |
| **Extranet** | พื้นที่เครือข่ายที่องค์กรเปิดให้คู่ค้า ลูกค้า หรือบุคคลภายนอกบางกลุ่มเข้าถึง | แยกจากระบบภายในอย่างไร ใครอนุมัติและยกเลิกสิทธิ์คู่ค้า |
| **LAN (Local Area Network)** | เครือข่ายในพื้นที่จำกัด เช่น สำนักงานหรืออาคาร | อุปกรณ์ใดต่อเข้าระบบได้ การแบ่ง VLAN และการควบคุม Port |
| **WAN (Wide Area Network)** | เครือข่ายที่เชื่อมหลายสำนักงานหรือหลายพื้นที่ | ความพร้อมใช้ ผู้ให้บริการ การเข้ารหัส และเส้นทางสำรอง |
| **Wireless/Wi-Fi** | การเชื่อมเครือข่ายแบบไร้สาย | แยก Guest Wi-Fi หรือไม่ ใช้การเข้ารหัสและ Authentication แบบใด |
| **VPN (Virtual Private Network)** | ช่องทางเข้ารหัสสำหรับเชื่อมต่อเครือข่ายจากระยะไกลหรือระหว่างสถานที่ | ใช้ MFA หรือไม่ ใครมีสิทธิ์ Log ครบหรือไม่ และบัญชีที่ไม่ใช้ถูกปิดหรือไม่ |
| **IP Address** | หมายเลขที่ใช้ระบุอุปกรณ์หรือปลายทางบนเครือข่าย | IP ใดเป็น Public/Private ใครเป็นเจ้าของ และ Log ระบุผู้ใช้ ณ เวลานั้นได้หรือไม่ |
| **Public IP** | IP ที่สื่อสารผ่านอินเทอร์เน็ตและมองเห็นได้จากภายนอก | มีบริการใดเปิดอยู่ มีการสแกนช่องโหว่และจำกัดแหล่งเข้าถึงหรือไม่ |
| **Private IP** | IP ที่ใช้ภายในเครือข่ายและไม่ได้ Route บนอินเทอร์เน็ตโดยตรง | การอยู่หลังเครือข่ายภายในไม่ได้แปลว่าปลอดภัย ต้องมี Access Control และ Monitoring |
| **MAC Address** | หมายเลขประจำ Network Interface ในระดับอุปกรณ์ | ใช้ช่วยระบุอุปกรณ์ได้ แต่ปลอมแปลงได้ จึงไม่ควรใช้เป็นหลักฐานยืนยันตัวตนเพียงอย่างเดียว |
| **Port** | หมายเลขช่องทางบริการบนอุปกรณ์ เช่น 443 สำหรับ HTTPS โดยทั่วไป | เปิดเฉพาะ Port ที่จำเป็นหรือไม่ ใครอนุมัติ และมีบริการไม่ปลอดภัยค้างอยู่หรือไม่ |
| **Protocol** | กติกาที่ระบบใช้สื่อสาร เช่น TCP/IP, HTTP, DNS | ใช้ Protocol รุ่นหรือรูปแบบที่ปลอดภัยหรือไม่ มี Protocol เก่าที่ส่งข้อมูลไม่เข้ารหัสหรือไม่ |
| **DNS (Domain Name System)** | ระบบแปลงชื่อ เช่น example.com ให้เป็น IP Address | ใครแก้ Record ได้ มีการป้องกันการแก้ไขมิชอบและมีระบบสำรองหรือไม่ |
| **DHCP** | บริการแจก IP และค่าเครือข่ายให้อุปกรณ์อัตโนมัติ | ระบุได้หรือไม่ว่าอุปกรณ์ใดได้ IP ใด ณ เวลาเกิดเหตุ และป้องกัน DHCP ปลอมอย่างไร |
| **Router** | อุปกรณ์ที่ส่งข้อมูลข้ามเครือข่ายหรือกำหนดเส้นทาง | Configuration, สิทธิ์ Admin, Firmware, Backup และเส้นทางสำรอง |
| **Switch** | อุปกรณ์เชื่อมต่อเครื่องในเครือข่ายเดียวกัน | VLAN, Port ที่ไม่ได้ใช้, Management access และ Configuration change |
| **VLAN** | การแบ่งเครือข่ายเชิงตรรกะบนอุปกรณ์เดียวกัน | แบ่ง User, Server, Guest และ Management เหมาะสมหรือไม่ และมี Route ข้ามเขตโดยใครอนุมัติ |
| **Network Segmentation** | การแบ่งเครือข่ายเป็นส่วนเพื่อลดการเข้าถึงและการลุกลาม | กฎการเชื่อมข้าม Segment สอดคล้องกับความจำเป็น และทดสอบจริงหรือไม่ |
| **DMZ (Demilitarized Zone)** | เขตเครือข่ายสำหรับระบบที่ต้องรับการเชื่อมต่อจากภายนอก โดยแยกจากระบบภายใน | ระบบ Public ถูกแยกจริงหรือไม่ และการเชื่อมต่อจาก DMZ เข้าภายในจำกัดเพียงใด |
| **Proxy** | ตัวกลางรับและส่งการเชื่อมต่อแทนผู้ใช้หรือ Server | บันทึกการใช้งาน กรองเว็บไซต์/ข้อมูล และป้องกันการหลีกเลี่ยงได้หรือไม่ |
| **Load Balancer** | กระจายคำขอไปยัง Server หลายเครื่อง | หากตัวหนึ่งเสียยังทำงานได้หรือไม่ การตั้งค่า Certificate/Session และ Health Check ถูกต้องหรือไม่ |
| **Bandwidth** | ปริมาณข้อมูลที่เครือข่ายรองรับได้ในช่วงเวลา | Capacity เพียงพอหรือไม่ มีการติดตามแนวโน้มและรับมือการใช้งานผิดปกติหรือ DDoS อย่างไร |
| **Latency** | เวลาหน่วงระหว่างส่งคำขอและรับผล | กระทบ SLA หรือกระบวนการสำคัญหรือไม่ และมี Baseline/Alert หรือไม่ |
| **Packet** | หน่วยข้อมูลย่อยที่ส่งผ่านเครือข่าย | Packet capture อาจมีข้อมูลสำคัญ ต้องควบคุมสิทธิ์และการเก็บรักษา |
| **NAT (Network Address Translation)** | การแปลง IP ระหว่างเครือข่ายภายในกับภายนอก | Log เพียงพอที่จะระบุต้นทางจริงหรือไม่ และกฎ NAT เปิดระบบเกินจำเป็นหรือไม่ |

## 2. การป้องกันเครือข่ายและความมั่นคงปลอดภัย

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Firewall** | อุปกรณ์หรือซอฟต์แวร์ที่อนุญาตหรือปฏิเสธการสื่อสารตามกฎ | Rule มีเจ้าของและเหตุผลหรือไม่ เปิดกว้างเกินจำเป็นหรือไม่ มีการทบทวน Log และ Rule หมดอายุหรือไม่ |
| **WAF (Web Application Firewall)** | Firewall ที่ช่วยกรองคำขอไปยัง Web Application | ครอบคลุมระบบใด อยู่ใน Blocking หรือ Monitoring mode และมีการติดตาม Alert/ข้อยกเว้นหรือไม่ |
| **IDS (Intrusion Detection System)** | ระบบตรวจจับพฤติกรรมที่อาจเป็นการโจมตีและแจ้งเตือน | Use case, coverage, tuning และการตอบสนองต่อ Alert |
| **IPS (Intrusion Prevention System)** | ระบบที่ตรวจจับและสามารถบล็อกการสื่อสารที่เป็นภัย | การบล็อกอาจกระทบระบบ ต้องดู Rule, exception, testing และ change control |
| **EDR (Endpoint Detection and Response)** | ระบบติดตาม ตรวจจับ และตอบสนองภัยบนเครื่องปลายทาง | ติดตั้งครอบคลุมหรือไม่ Agent ทำงานและอัปเดตหรือไม่ Alert ถูกติดตามหรือไม่ |
| **XDR (Extended Detection and Response)** | รวมข้อมูลภัยจากหลายแหล่ง เช่น Endpoint, Email, Identity และ Network | การเชื่อมข้อมูลครอบคลุมและ Use case ให้ผลที่ทีมตอบสนองได้จริงหรือไม่ |
| **Antivirus/Anti-malware** | โปรแกรมตรวจจับและป้องกันมัลแวร์ | Coverage, Update, Policy, Detection และเครื่องที่ปิด/ล้าสมัย |
| **SIEM (Security Information and Event Management)** | ระบบรวม Log เพื่อค้นหาเหตุผิดปกติและแจ้งเตือน | มี Log Source สำคัญครบหรือไม่ เวลาตรงกัน Use case ใช้งานได้ และทีมจัดการ Alert ทันเวลาหรือไม่ |
| **SOC (Security Operations Center)** | ทีม/ศูนย์ที่เฝ้าระวัง วิเคราะห์ และตอบสนองเหตุความปลอดภัย | Operating model, coverage, SLA, escalation, ทักษะ และคุณภาพ Case closure |
| **DLP (Data Loss Prevention)** | Control ที่ตรวจหรือป้องกันข้อมูลสำคัญถูกส่งออกโดยไม่เหมาะสม | นิยามข้อมูล Rule, ช่องทางที่ครอบคลุม, false positive, exception และ incident handling |
| **NAC (Network Access Control)** | ระบบควบคุมว่าอุปกรณ์ใดเข้าเครือข่ายได้ | ตรวจตัวตนและสภาพเครื่องอย่างไร Guest/IoT แยกหรือไม่ และมี bypass ใด |
| **Zero Trust** | แนวคิดไม่ให้ความเชื่อถือจากตำแหน่งเครือข่ายเพียงอย่างเดียว ต้องตรวจสอบอย่างต่อเนื่อง | อย่าตรวจแค่ว่ามีนโยบายชื่อ Zero Trust ให้ดู Identity, device, least privilege, segmentation และ monitoring จริง |
| **Defense in Depth** | ใช้ Control หลายชั้นเพื่อไม่พึ่งมาตรการเดียว | แต่ละชั้นจัดการความเสี่ยงอะไร มีช่องว่างหรือ Control ซ้ำซ้อนโดยไม่เพิ่มคุณค่าหรือไม่ |
| **Hardening** | ปรับระบบให้ปลอดภัยขึ้น เช่น ปิด Service/Account ที่ไม่ใช้ | มี Approved baseline, exception และการตรวจ Configuration drift หรือไม่ |
| **Security Baseline** | ค่าตั้งต้นความปลอดภัยที่องค์กรอนุมัติ | อ้างอิงรุ่นระบบที่ถูกต้อง มีการทบทวน และตรวจ Compliance อย่างไร |
| **Vulnerability** | จุดอ่อนที่อาจถูกใช้ก่อความเสียหาย | พบจากแหล่งใด ผูกกับ Asset/Business impact และแก้ตาม SLA หรือไม่ |
| **Vulnerability Assessment (VA)** | กระบวนการค้นหาและประเมินช่องโหว่ | Scope, credentialed scan, ความครบถ้วน Asset, false positive, remediation และ rescan |
| **Penetration Test (PT)** | การทดสอบโดยจำลองการโจมตีเพื่อพิสูจน์การใช้ประโยชน์จากช่องโหว่ตามขอบเขต | ผู้อนุมัติ ขอบเขต Rules of Engagement ผลกระทบ การเก็บหลักฐาน การแก้และ Retest |
| **CVE** | รหัสระบุช่องโหว่ที่เปิดเผยต่อสาธารณะ | ระบบขององค์กรใช้ผลิตภัณฑ์/Version ที่ได้รับผลจริงหรือไม่ ไม่สรุปจากชื่อผลิตภัณฑ์อย่างเดียว |
| **CVSS** | คะแนนเชิงเทคนิคสำหรับช่วยประเมินความรุนแรงของช่องโหว่ | ต้องพิจารณา Business context, exposure และ existing control เพิ่ม ไม่ใช้คะแนนเป็น Risk rating โดยอัตโนมัติ |
| **Patch** | ชุดแก้ข้อบกพร่องหรือช่องโหว่ของซอฟต์แวร์ | ความครบถ้วน รอบเวลา การทดสอบ การนำขึ้นระบบ ข้อยกเว้น และหลักฐานหลังติดตั้ง |
| **Exploit** | วิธีหรือโค้ดที่ใช้ประโยชน์จากช่องโหว่ | มีการใช้งานจริงหรือไม่ ระบบเปิดรับจากที่ใด และ Control ลดโอกาส/ผลกระทบเพียงใด |
| **Malware** | ซอฟต์แวร์มุ่งร้าย เช่น Virus, Worm, Trojan และ Spyware | ช่องทางเข้า การป้องกัน การตรวจจับ การแยกระบบ และ Recovery |
| **Ransomware** | มัลแวร์ที่เข้ารหัส/ขโมยข้อมูลเพื่อเรียกค่าไถ่ | MFA, segmentation, EDR, privileged access, Backup แบบแยก/แก้ไม่ได้, exercise และ incident response |
| **Phishing** | การหลอกให้เปิดเผยข้อมูล คลิกลิงก์ หรือทำรายการ | Email control, awareness, reporting channel, simulation และการตอบสนองต่อบัญชีที่ถูกขโมย |
| **Social Engineering** | การหลอกบุคคลเพื่อข้าม Control ทางเทคนิคหรือกระบวนการ | Help Desk, payment change, visitor และ account recovery มีการยืนยันผ่านช่องทางอิสระหรือไม่ |
| **DDoS** | การส่งคำขอจำนวนมากจากหลายแหล่งเพื่อทำให้บริการใช้ไม่ได้ | Capacity, protection service, runbook, monitoring, provider coordination และ test |
| **MITM (Man-in-the-Middle)** | ผู้โจมตีแทรกกลางเพื่ออ่านหรือเปลี่ยนข้อมูล | Encryption, certificate validation, secure Wi-Fi และการป้องกันการลดระดับ Protocol |
| **IOC (Indicator of Compromise)** | ร่องรอยที่อาจบอกว่าถูกโจมตี เช่น IP, Domain หรือ File Hash | แหล่งที่มา ความสด ความเกี่ยวข้อง การนำไปค้นหา/บล็อก และผลลัพธ์ที่ติดตาม |
| **TTP (Tactics, Techniques and Procedures)** | รูปแบบเป้าหมาย วิธี และขั้นตอนที่ผู้โจมตีใช้ | องค์กรนำข้อมูล TTP ไปปรับ Detection, Control และ Exercise ที่เกี่ยวกับภัยจริงหรือไม่ |
| **Threat Intelligence** | ข้อมูลภัยที่ผ่านการวิเคราะห์เพื่อช่วยตัดสินใจ | มีคำถามข่าวกรอง ผู้ใช้ข้อมูล แหล่งที่น่าเชื่อถือ Action และการวัดผลหรือไม่ |
| **Threat Modeling** | การมองระบบ/ธุรกิจเพื่อระบุว่าอะไรสำคัญ อะไรอาจผิดพลาด และจะจัดการอย่างไร | ขอบเขต Asset, data flow, trust boundary, scenario, prioritization และการทบทวนเมื่อระบบเปลี่ยน |

## 3. เครื่องแม่ข่าย ระบบปฏิบัติการ และโครงสร้างพื้นฐาน

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Server** | เครื่องหรือบริการที่ให้ทรัพยากรแก่ระบบอื่น เช่น Web, Database หรือ File Server | เจ้าของระบบ Version, hardening, patch, access, monitoring, backup และความพร้อมใช้ |
| **Physical Server** | Server ที่ทำงานบนเครื่องจริงโดยตรง | สถานที่ อุปกรณ์สำรอง Capacity Warranty และการกำจัดสื่อ |
| **Virtual Machine (VM)** | เครื่องเสมือนที่ทำงานบน Hardware ร่วมกับ VM อื่น | ใครสร้าง/Clone/Snapshot ได้ การแบ่งทรัพยากร และการป้องกัน Management layer |
| **Hypervisor** | ซอฟต์แวร์ที่สร้างและบริหาร VM | เป็นจุดควบคุมสำคัญ ต้องจำกัดสิทธิ์ Patch และ Monitor |
| **Operating System (OS)** | ซอฟต์แวร์หลักที่ควบคุม Hardware และรองรับ Application เช่น Windows/Linux | Version/EOL, account, patch, service, logging, hardening และ privilege |
| **Database (DB)** | ระบบจัดเก็บและจัดการข้อมูลอย่างมีโครงสร้าง | สิทธิ์ DBA/ผู้ใช้ การเข้ารหัส Audit log Backup การเปลี่ยน Schema และการเข้าถึงข้อมูล Production |
| **DBMS** | ซอฟต์แวร์บริหารฐานข้อมูล เช่น Oracle, SQL Server หรือ PostgreSQL | Version, authentication mode, privileged role, patch และ configuration |
| **Schema** | โครงสร้างเชิงตรรกะของตาราง มุมมอง และวัตถุในฐานข้อมูล | การเปลี่ยน Schema ได้รับอนุมัติ ทดสอบ และตรวจย้อนหลังได้หรือไม่ |
| **Table** | โครงสร้างเก็บข้อมูลเป็นแถวและคอลัมน์ | ความหมายของ Field, key, completeness และสิทธิ์อ่าน/แก้ข้อมูล |
| **SQL** | ภาษาสำหรับค้นหาและจัดการข้อมูลในฐานข้อมูล | Query ที่ใช้ตรวจต้องได้รับอนุญาต ระบุเงื่อนไขครบ และไม่เปลี่ยน Production โดยไม่ตั้งใจ |
| **Middleware** | ซอฟต์แวร์ตัวกลางที่ช่วยให้ระบบต่างกันสื่อสารกัน | Version, access, interface configuration, queue/error และ monitoring |
| **Container** | หน่วยรัน Application ที่รวม Code และ Dependency เช่น Docker container | Image source, vulnerability, secret, privilege, configuration และ orchestration access |
| **Kubernetes** | ระบบจัดการ Container จำนวนมาก | Cluster/admin access, namespace, network policy, secret, image admission, logging และ backup configuration |
| **Data Center** | สถานที่และโครงสร้างพื้นฐานสำหรับระบบ IT จำนวนมาก | Physical/environmental control, redundancy, access, maintenance, capacity และ DR |
| **Server Room** | ห้องเก็บ Server ภายในองค์กร ขนาดมักเล็กกว่า Data Center | ทางเข้า อุณหภูมิ ไฟฟ้า น้ำ/ไฟ สายสัญญาณ การเฝ้าระวังและสิ่งของที่ไม่ควรอยู่ในห้อง |
| **Rack** | ตู้หรือโครงสำหรับติดตั้ง Server และอุปกรณ์เครือข่าย | ล็อก การจัดสาย ป้ายกำกับ อุปกรณ์หนัก/ร้อน และการเข้าถึง |
| **UPS (Uninterruptible Power Supply)** | แหล่งไฟชั่วคราวเมื่อไฟหลักขัดข้อง ช่วยให้ระบบทำงานต่อช่วงหนึ่งหรือปิดอย่างปลอดภัย | Capacity, battery life, maintenance, alarm และผล Load/Failover test; UPS ไม่ใช่ Generator |
| **Generator** | เครื่องกำเนิดไฟฟ้าสำรองสำหรับเหตุไฟดับนานกว่า UPS รองรับ | เชื้อเพลิง การบำรุงรักษา การทดสอบภายใต้ Load และเวลาที่เริ่มจ่ายไฟ |
| **Redundancy** | มีอุปกรณ์หรือเส้นทางสำรองเพื่อลด Single Point of Failure | สำรองจริงและแยก Failure domain หรือไม่ มีการทดสอบ Failover หรือเป็นเพียงอุปกรณ์ที่ไม่ได้พร้อมใช้ |
| **High Availability (HA)** | การออกแบบให้บริการหยุดน้อย โดยสลับไปส่วนสำรองได้ | Architecture, health check, failover time, data consistency และผลทดสอบ |
| **Failover** | การสลับการทำงานจากส่วนหลักไปส่วนสำรอง | ทำอัตโนมัติหรือ Manual ใครอนุมัติ ใช้เวลาจริงเท่าใด และเคยทดสอบหรือไม่ |
| **Single Point of Failure (SPOF)** | จุดเดียวที่เสียแล้วทำให้บริการทั้งส่วนหยุด | ระบุครบหรือไม่ ยอมรับความเสี่ยงหรือมี Redundancy/Workaround |
| **Capacity** | ความสามารถของระบบในการรองรับปริมาณงาน | มี Threshold, forecast และแผนเพิ่มทรัพยากรก่อนกระทบบริการหรือไม่ |
| **End of Life/End of Support (EOL/EOS)** | วันที่ผู้ผลิตหยุดขายหรือหยุดสนับสนุน/แก้ช่องโหว่ | Inventory, upgrade plan, compensating control และ risk acceptance |
| **Asset Inventory/CMDB** | รายการทรัพย์สินและความสัมพันธ์ของระบบ/อุปกรณ์/ซอฟต์แวร์ | ครบ ถูก ปัจจุบัน มี Owner และ Criticality หรือไม่ เพราะ Control อื่นพึ่งพารายการนี้ |

## 4. Application, API และการแลกเปลี่ยนข้อมูล

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Application** | โปรแกรมที่ช่วยผู้ใช้ทำกระบวนการธุรกิจ | Owner, business rule, access, change, interface, data และ continuity |
| **Web Application** | Application ที่ใช้งานผ่าน Web Browser | Authentication, session, input validation, access control, API, vulnerability และ logging |
| **Mobile Application** | Application บนโทรศัพท์หรืออุปกรณ์พกพา | Version, secure storage, permission, lost device, API และการรองรับรุ่นเก่า |
| **ERP (Enterprise Resource Planning)** | ระบบรวมหลายกระบวนการ เช่น ขาย ซื้อ สต็อก บัญชี และผลิต | Configuration, master data, SoD, interface และผลกระทบข้ามกระบวนการ |
| **API (Application Programming Interface)** | ช่องทางที่ระบบให้ระบบอื่นเรียกใช้ข้อมูลหรือความสามารถตามรูปแบบที่กำหนด | ใครเรียกได้ สิทธิ์ระดับใด ตรวจ Input อย่างไร จำกัดปริมาณหรือไม่ Version/Log และข้อมูลตอบกลับเกินจำเป็นหรือไม่ |
| **Endpoint (API)** | URL หรือจุดบริการเฉพาะของ API | เปิดสู่ใคร ใช้ Method ใด Authentication/Authorization ถูกต้อง และมี Inventory หรือไม่ |
| **Interface** | จุดหรือกระบวนการเชื่อมข้อมูลระหว่างระบบ อาจเป็น API, File, Queue หรือ Manual upload | ความครบถ้วน ความถูกต้อง Duplicate, error/retry, reconciliation และ Owner ทั้งสองฝั่ง |
| **Integration** | การทำให้หลายระบบทำงานหรือแลกข้อมูลร่วมกัน | Dependency, failure handling, shared responsibility และการเปลี่ยนระบบหนึ่งกระทบอีกระบบอย่างไร |
| **Webhook** | การที่ระบบหนึ่งส่งข้อความอัตโนมัติไปยังอีกระบบเมื่อมีเหตุการณ์ | ยืนยันผู้ส่ง Secret/signature, retry, duplicate และข้อมูลสำคัญใน Payload |
| **Message Queue** | พื้นที่พักข้อความเพื่อให้ระบบส่งและรับแบบไม่ต้องทำพร้อมกัน | ข้อความตกค้าง สูญหาย ซ้ำ ลำดับผิด Dead-letter queue และ Monitoring |
| **Batch** | การรวบรวมรายการหลายรายการมาประมวลผลเป็นรอบ | Schedule, completeness, control total, failed/restart และ Cut-off |
| **Real-time Processing** | ประมวลผลทันทีหรือใกล้ทันทีเมื่อเกิดรายการ | Availability, latency, duplicate, timeout และวิธีคืนสถานะเมื่อบางขั้นตอนล้มเหลว |
| **ETL (Extract, Transform, Load)** | ดึงข้อมูล แปลงรูป และนำเข้าอีกระบบ/คลังข้อมูล | Mapping, transformation rule, reject, control total, lineage และ change control |
| **File Transfer/SFTP** | การส่งไฟล์ระหว่างระบบ โดย SFTP เป็นช่องทางเข้ารหัสรูปแบบหนึ่ง | Encryption, key/account, folder permission, naming, completeness, retention และ failed transfer |
| **Input Validation** | การตรวจข้อมูลนำเข้าว่าครบ รูปแบบถูก และอยู่ในค่าที่รับได้ | ตรวจทั้งฝั่ง Server ไม่พึ่ง Browser อย่างเดียว และมี error handling ที่เหมาะสม |
| **Edit Check** | กฎตรวจข้อมูล เช่น Range, format, existence หรือ duplicate | กฎตรงกับนโยบายธุรกิจหรือไม่ ครอบคลุม boundary และใครแก้ configuration ได้ |
| **Business Rule** | เงื่อนไขที่กำหนดว่าระบบต้องทำงานอย่างไร | ได้รับอนุมัติ ตีความตรงกัน แปลงเป็น configuration/code ถูก และมี expected result |
| **Workflow** | ลำดับขั้นตอนและผู้ดำเนินการ/อนุมัติในระบบ | Threshold, delegation, bypass, maker-checker และ audit trail |
| **Master Data** | ข้อมูลหลักที่ใช้ซ้ำ เช่น ลูกค้า ผู้ขาย สินค้า ราคา และผังบัญชี | การสร้าง/แก้/ยกเลิก สิทธิ์ อนุมัติ Duplicate และ change log |
| **Transaction Data** | ข้อมูลเหตุการณ์ทางธุรกิจ เช่น ใบสั่งซื้อ การขาย หรือการจ่ายเงิน | Validity, completeness, accuracy, authorization, cut-off และ duplicate |
| **Source Code** | คำสั่งต้นฉบับที่นักพัฒนาเขียน | Repository access, review, change traceability, secret และการนำขึ้น Production |
| **Object Code/Executable** | โปรแกรมที่ถูกแปลงให้เครื่องรันได้ | Build จาก Source ที่อนุมัติหรือไม่ Integrity และการควบคุม Deployment |
| **Configuration** | ค่าที่กำหนดพฤติกรรมระบบโดยไม่แก้ Source Code โดยตรง | Configuration อาจเปลี่ยนผลธุรกิจได้ จึงต้องมี Owner, approval, testing และ log |
| **Environment** | สภาพแวดล้อมระบบ เช่น Development, Test, UAT และ Production | แยกสิทธิ์/ข้อมูลหรือไม่ การย้ายข้าม Environment ถูกควบคุมหรือไม่ |
| **Production** | ระบบจริงที่ให้บริการหรือประมวลผลข้อมูลจริง | จำกัดสิทธิ์ การเปลี่ยน การใช้ข้อมูล และ Monitoring เข้มกว่าสภาพแวดล้อมอื่น |
| **UAT (User Acceptance Testing)** | การทดสอบโดยฝ่ายธุรกิจว่าระบบตอบความต้องการก่อนใช้งานจริง | ผู้ทดสอบเหมาะสม Test case ครอบคลุม Expected result ชัด และข้อผิดพลาดถูกแก้ก่อนอนุมัติหรือไม่ |
| **Regression Testing** | ทดสอบว่าส่วนที่เคยทำงานยังทำงานหลังมีการเปลี่ยน | Scope อิงผลกระทบ และไม่ใช้แทนการทดสอบ Feature ใหม่ทั้งหมด |
| **Reconciliation** | การกระทบยอดสองแหล่งเพื่อค้นหาความต่าง | แหล่งทั้งสองเป็นอิสระพอหรือไม่ ใครตรวจ ความต่างถูกติดตาม และข้อมูลครบหรือไม่ |
| **Control Total** | ยอดควบคุม เช่น จำนวนรายการหรือยอดเงินรวม ใช้เทียบก่อนและหลังประมวลผล | สร้างจากแหล่งใด ป้องกันการแก้ และมีผู้ติดตาม Difference หรือไม่ |

## 5. Identity, Account และการควบคุมสิทธิ์

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Identity** | ตัวตนดิจิทัลของบุคคล บริการ หรืออุปกรณ์ | ผูกกับเจ้าของจริง มีวงจรสร้าง-เปลี่ยน-ยกเลิก และตรวจย้อนหลังได้หรือไม่ |
| **Account/User ID** | ชื่อบัญชีที่ใช้เข้าระบบ | เป็นบัญชีรายบุคคลหรือ Shared มี Owner/สถานะ และปิดเมื่อไม่ใช้หรือไม่ |
| **Authentication** | การพิสูจน์ว่าเป็นตัวตนที่กล่าวอ้าง | วิธีพิสูจน์เหมาะกับความเสี่ยง รวม Enrollment และ Recovery ไม่ใช่เฉพาะ Login |
| **Authorization** | การกำหนดว่าตัวตนที่ผ่านการพิสูจน์แล้วทำอะไรได้ | สิทธิ์ตรงกับหน้าที่ ผ่านอนุมัติ และทบทวนหรือไม่ |
| **MFA (Multi-Factor Authentication)** | ใช้ปัจจัยยืนยันคนละประเภทมากกว่าหนึ่ง เช่น สิ่งที่รู้และสิ่งที่มี | ครอบคลุมระบบ/บัญชีสำคัญหรือไม่ มี bypass/recovery ที่อ่อนกว่า Login หรือไม่ |
| **SSO (Single Sign-On)** | เข้าสู่ระบบครั้งเดียวแล้วใช้หลาย Application | ลดบัญชีซ้ำได้ แต่ Identity Provider เป็นจุดสำคัญ ต้องดู MFA, availability, access และ logging |
| **IAM (Identity and Access Management)** | กระบวนการและระบบบริหารตัวตนและสิทธิ์ | Joiner-Mover-Leaver, role, approval, review, privileged account และ orphan account |
| **PAM (Privileged Access Management)** | ระบบ/กระบวนการควบคุมบัญชีสิทธิ์สูง | Vault, checkout, approval, session recording, password rotation, emergency access และ coverage |
| **Privileged Account** | บัญชีที่มีอำนาจสูง เช่น Admin, Root หรือ DBA | มีเท่าที่จำเป็น แยกจากบัญชีใช้งานปกติ และทุกกิจกรรมระบุตัวบุคคลได้หรือไม่ |
| **Service Account** | บัญชีที่ Application หรือบริการใช้สื่อสาร/ทำงานอัตโนมัติ | Owner, purpose, noninteractive use, secret rotation, privilege และบัญชีที่ไม่มีระบบใช้แล้ว |
| **Shared Account** | บัญชีที่หลายคนใช้ร่วมกัน | Accountability ต่ำ ควรหลีกเลี่ยงหรือมี compensating control ที่ระบุตัวผู้ใช้จริงได้ |
| **Default Account** | บัญชีที่ติดมากับระบบ เช่น admin/guest | เปลี่ยนรหัส ปิด เปลี่ยนชื่อ หรือควบคุมตามความเหมาะสมหรือไม่ |
| **RBAC (Role-Based Access Control)** | ให้สิทธิ์ตาม Role หรืองาน แทนกำหนดรายคนทุกสิทธิ์ | Role design, owner, toxic combination, role creep และ review |
| **Least Privilege** | ให้สิทธิ์เท่าที่ต้องใช้เพื่อทำงาน | ตรวจ Effective permission ไม่ใช่ชื่อ Role อย่างเดียว |
| **Need to Know** | ให้เข้าถึงข้อมูลเมื่อจำเป็นต่อหน้าที่ | ใช้เสริม Least Privilege โดยเฉพาะข้อมูลลับและข้อมูลส่วนบุคคล |
| **SoD (Segregation of Duties)** | แยกหน้าที่ที่ขัดกันไม่ให้คนเดียวควบคุมครบวงจร | Matrix, conflict, transaction จริง, exception และ compensating review |
| **Maker-Checker** | คนหนึ่งจัดทำ อีกคนตรวจ/อนุมัติ | Checker เป็นอิสระ มีอำนาจ/ข้อมูลเพียงพอ และระบบห้ามอนุมัติของตนเองหรือไม่ |
| **Joiner-Mover-Leaver (JML)** | วงจรให้สิทธิ์พนักงานเข้าใหม่ เปลี่ยนงาน และออกจากงาน | Trigger จาก HR, SLA, ระบบที่ครอบคลุม, temporary access และ reconciliation |
| **Access Review/Recertification** | การให้ Owner ทบทวนเป็นระยะว่าใครควรมีสิทธิ์ใดต่อ | Population ครบ Reviewer เข้าใจสิทธิ์ ตัดสินใจจริง และ Remove ตามผลทันเวลาหรือไม่ |
| **Password Policy** | กฎเกี่ยวกับรหัสผ่าน เช่น ความยาว การใช้ซ้ำ และ Lockout | ใช้จริงตรง Policy หรือไม่ ครอบคลุม Service/privileged account และสอดคล้องกับ Authentication อื่นหรือไม่ |
| **Secret** | ข้อมูลลับที่ระบบใช้ยืนยัน เช่น API key, token หรือ private key | ไม่ฝังใน Source Code จัดเก็บใน Vault จำกัดสิทธิ์ หมุนเวียน และยกเลิกเมื่อรั่วหรือไม่ |
| **Session** | สถานะหลัง Login ที่ทำให้ระบบจำผู้ใช้ในช่วงหนึ่ง | Timeout, token protection, logout, concurrent session และการยกเลิกเมื่อความเสี่ยงเปลี่ยน |

## 6. ข้อมูล การเข้ารหัส และความเป็นส่วนตัว

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Data** | ข้อเท็จจริงหรือค่าที่ระบบจัดเก็บและประมวลผล | Owner, classification, quality, access, flow, retention และ disposal |
| **Information Asset** | ข้อมูล ระบบ บุคลากร หรือทรัพยากรที่มีคุณค่าต่อองค์กร | Inventory, owner, criticality และ Control ตามระดับความสำคัญ |
| **Data Classification** | การแบ่งระดับข้อมูล เช่น Public, Internal, Confidential และ Restricted | นิยามชัด ใช้ Label จริง และ Control สอดคล้องกับระดับหรือไม่ |
| **Data Owner** | ผู้รับผิดชอบเชิงธุรกิจในการตัดสินใจเรื่องข้อมูล | อนุมัติสิทธิ์ คุณภาพ การใช้ การเก็บ และการเปิดเผยจริงหรือไม่ |
| **Data Custodian** | ผู้ดูแลทางเทคนิคตามคำสั่ง/นโยบายของ Owner | บริหาร Storage, Backup และ Security โดยไม่ตัดสินวัตถุประสงค์ใช้ข้อมูลแทน Owner |
| **Data Flow** | เส้นทางที่ข้อมูลเคลื่อนจากแหล่งหนึ่งไปอีกแหล่ง | มีจุดออกนอกองค์กร Trust boundary การเข้ารหัส และระบบที่ไม่อยู่ใน Inventory หรือไม่ |
| **Data Lineage** | ประวัติว่าข้อมูลมาจากไหน ผ่านการแปลงอะไร และไปอยู่ที่ใด | รายงานสำคัญตามกลับต้นทางได้ และ Change ต่อ Transformation ถูกควบคุมหรือไม่ |
| **Data Quality** | ระดับที่ข้อมูลถูกต้อง ครบ ตรงเวลา สอดคล้อง และเหมาะกับการใช้ | มี Rule, Owner, threshold, issue remediation และ monitoring หรือไม่ |
| **PII/Personal Data** | ข้อมูลที่เกี่ยวกับหรือระบุตัวบุคคลได้ตามบริบทและกฎหมายที่ใช้ | Inventory, lawful use, minimization, access, retention, transfer และ incident |
| **Encryption** | การแปลงข้อมูลให้อ่านไม่ได้หากไม่มีกุญแจ | ครอบคลุม Data at Rest/In Transit, algorithm/configuration, key access และ rotation |
| **Data at Rest** | ข้อมูลขณะจัดเก็บ เช่น ใน Database, Disk หรือ Backup | Encryption, access, backup และ media disposal |
| **Data in Transit** | ข้อมูลขณะส่งผ่าน Network หรือ Interface | Protocol, certificate, endpoint validation และ downgrade/legacy connection |
| **Cryptographic Key** | กุญแจที่ใช้เข้ารหัส ถอดรหัส หรือสร้างลายมือชื่อ | Generation, storage, access, backup, rotation, expiry, revocation และ separation of duties |
| **Hash** | ค่าที่คำนวณจากข้อมูลเพื่อช่วยตรวจการเปลี่ยนแปลง โดยทั่วไปย้อนกลับไม่ได้แบบการถอดรหัส | Algorithm ที่เหมาะสม การใช้ตรวจ Integrity และ Salt สำหรับ Password |
| **Digital Certificate** | เอกสารดิจิทัลที่ผูก Public Key กับตัวตนและออกโดยผู้รับรอง | Issuer, hostname, validity, expiry, private key protection และ renewal |
| **TLS/HTTPS** | Protocol เข้ารหัสการสื่อสารระหว่างระบบ โดย HTTPS คือ HTTP ผ่าน TLS | Version/cipher, certificate validation, expiry และครอบคลุมทุกเส้นทางที่มีข้อมูลสำคัญหรือไม่ |
| **Token** | ข้อมูลที่ใช้แทนสิทธิ์หรือ Session เพื่อเรียกบริการ | Scope, lifetime, storage, revocation, audience และไม่ปรากฏใน Log โดยไม่จำเป็น |
| **Masking** | ปิดบังข้อมูลบางส่วน เช่น แสดงเลขบัตรเพียงท้ายสี่หลัก | Mask ในหน้าจอ Export Log และ Non-production ครบหรือไม่ และย้อนกลับได้โดยใคร |
| **Anonymization** | ทำข้อมูลให้ไม่สามารถเชื่อมกลับไปหาบุคคลได้อย่างมีประสิทธิผล | ความเสี่ยง Re-identification และข้อมูลประกอบอื่นที่อาจเชื่อมกลับได้ |
| **Retention** | ระยะเวลาที่ต้องเก็บข้อมูล | มีเกณฑ์ทางธุรกิจ/กฎหมาย ระบบทำตามจริง และมี Legal hold/exception หรือไม่ |
| **Secure Disposal** | การทำลายข้อมูลหรือสื่อให้กู้คืนไม่ได้ตามระดับความเสี่ยง | วิธีทำ ผู้อนุมัติ Certificate/log และครอบคลุม Backup/Cloud/อุปกรณ์คืน Vendor หรือไม่ |

## 7. Log, Monitoring และการจัดการเหตุการณ์

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Event** | เหตุการณ์ใดๆ ที่ระบบบันทึก เช่น Login หรือ Service start | Event ใดสำคัญต่อความเสี่ยง และถูกส่งไปตรวจหรือไม่ |
| **Log** | บันทึกรายละเอียดเหตุการณ์ของระบบ Application หรืออุปกรณ์ | บันทึกใคร ทำอะไร เมื่อใด จากที่ใด ผลเป็นอย่างไร ครบ ถูกป้องกัน และเก็บนานพอหรือไม่ |
| **Audit Trail** | ร่องรอยที่ช่วยตามลำดับกิจกรรมหรือการเปลี่ยนข้อมูลย้อนหลัง | มีค่า Before/After, User, timestamp และ Transaction ID หรือไม่ และผู้ทำแก้ร่องรอยตนเองได้หรือไม่ |
| **Timestamp** | วันและเวลาที่กำกับเหตุการณ์ | ระบบใช้ Time source เดียวกัน Time zone ชัด และเวลาไม่คลาดจนต่อ Timeline ไม่ได้ |
| **NTP (Network Time Protocol)** | บริการทำเวลาอุปกรณ์ให้ตรงกัน | แหล่งเวลา การครอบคลุม และ Alert เมื่อ Sync ไม่สำเร็จ |
| **Monitoring** | การเฝ้าดูสถานะ ประสิทธิภาพ หรือภัยของระบบ | Coverage, threshold, owner, เวลาให้บริการ และการตอบสนอง |
| **Alert** | การแจ้งเตือนเมื่อพบเงื่อนไขที่กำหนด | Alert ไปถึงใคร ความสำคัญถูกจัดหรือไม่ False positive และ Alert ค้าง |
| **False Positive** | ระบบแจ้งว่าเป็นปัญหาแต่ตรวจแล้วไม่ใช่ | มี tuning โดยไม่ปิดการตรวจจับสำคัญ และบันทึกเหตุผลหรือไม่ |
| **False Negative** | มีปัญหาจริงแต่ระบบไม่แจ้ง | ประเมินยาก ต้องใช้ exercise, incident retrospective และ coverage review |
| **Incident** | เหตุที่กระทบหรืออาจกระทบความลับ ความถูกต้อง หรือความพร้อมใช้ | Classification, owner, containment, recovery, communication, evidence และ lesson learned |
| **Problem Management** | การหาและจัดการสาเหตุของ Incident ที่เกิดซ้ำหรือมีนัยสำคัญ | RCA มีคุณภาพ Action แก้ต้นเหตุ และติดตามประสิทธิผลหรือไม่ |
| **Ticket** | รายการงานในระบบติดตาม เช่น Incident, Request หรือ Change | Population ครบ สถานะ/เวลาแก้เชื่อถือได้ Approval และ closure evidence |
| **SLA (Service Level Agreement)** | ข้อตกลงระดับบริการ เช่น เวลาให้บริการและเวลาแก้เหตุ | Metric นิยามชัด แหล่งข้อมูลถูกต้อง มีข้อยกเว้นและบทลงโทษ/การติดตามหรือไม่ |
| **KPI** | ตัวชี้วัดผลการดำเนินงาน | เชื่อมเป้าหมาย คำนวณจากข้อมูลเชื่อถือได้ และไม่สร้างแรงจูงใจผิด |
| **KRI** | ตัวชี้วัดแนวโน้มหรือระดับความเสี่ยง | Threshold, owner, escalation และนำไปตัดสินใจจริงหรือไม่ |
| **Root Cause Analysis (RCA)** | การวิเคราะห์สาเหตุรากของปัญหา | แยกอาการจากสาเหตุ มีหลักฐาน และ Action ลดโอกาสเกิดซ้ำหรือไม่ |
| **Chain of Custody** | บันทึกว่าใครครอบครองหรือจัดการหลักฐานเมื่อใด | ใช้เมื่อหลักฐานอาจนำไปสืบสวนหรือคดี ต้องรักษา Integrity และการส่งมอบ |

## 8. Backup, Continuity และ Disaster Recovery

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Backup** | สำเนาข้อมูลสำหรับกู้คืน | Backup สำเร็จไม่ได้แปลว่ากู้ได้ ต้องตรวจ Restore, coverage, RPO, access และ isolation |
| **Full Backup** | สำรองข้อมูลทั้งหมดในขอบเขต | เวลา/พื้นที่มากแต่ Recovery มักตรงไปตรงมากว่า ต้องดู Schedule และความครบถ้วน |
| **Incremental Backup** | สำรองเฉพาะส่วนที่เปลี่ยนจาก Backup ครั้งล่าสุด | ใช้พื้นที่น้อย แต่ Recovery พึ่งหลายชุด ต้องทดสอบลำดับและความครบถ้วน |
| **Differential Backup** | สำรองส่วนที่เปลี่ยนตั้งแต่ Full Backup ล่าสุด | Recovery ใช้ Full และ Differential ล่าสุด โดยต้องตรวจกลยุทธ์และผลทดสอบจริง |
| **Snapshot** | ภาพสถานะของข้อมูล/VM ณ จุดเวลา | อาจอยู่บน Storage เดียวกับระบบหลัก จึงไม่ใช่ Backup ที่แยกจากภัยทุกกรณี |
| **Restore** | การนำข้อมูลจาก Backup กลับมา | ทดสอบข้อมูลครบ ใช้งานได้ สิทธิ์ถูก และเวลา/จุดข้อมูลตรงเป้าหมายหรือไม่ |
| **BCM (Business Continuity Management)** | การบริหารให้องค์กรดำเนินงานสำคัญต่อได้เมื่อถูกรบกวน | Governance, BIA, strategy, plan, exercise และ improvement ครอบคลุมคน สถานที่ คู่ค้า และ IT |
| **BCP (Business Continuity Plan)** | แผนให้กระบวนการธุรกิจดำเนินต่อระหว่างเหตุ | Workaround, people, communication, dependency และทรัพยากร ไม่จำกัดเฉพาะการกู้ Server |
| **DR (Disaster Recovery)** | การกู้ระบบ IT และข้อมูลหลังเหตุร้ายแรง | Architecture, priority, dependency, procedure, access, communication และ test |
| **DRP (Disaster Recovery Plan)** | เอกสารกำหนดวิธีกู้ระบบ IT | Owner, version, contact, step, dependency, RTO/RPO และผล exercise |
| **BIA (Business Impact Analysis)** | วิเคราะห์ว่ากระบวนการหยุดแล้วกระทบอะไรและทนนานเท่าใด | Business owner มีส่วนร่วม สมมติฐาน/Dependency ครบ และเชื่อมไป Recovery priority จริงหรือไม่ |
| **RTO (Recovery Time Objective)** | เวลาเป้าหมายในการฟื้นบริการหลังหยุดชะงัก | จุดเริ่ม/จบการวัดชัด และเวลาทดสอบจริงรวมการทำให้ธุรกิจใช้ได้หรือไม่ |
| **RPO (Recovery Point Objective)** | ปริมาณข้อมูลย้อนหลังสูงสุดที่ยอมสูญเสียได้ วัดเป็นเวลา | Backup/replication frequency และผล Recovery รองรับเป้าหมายจริงหรือไม่ |
| **MTPD/MTD** | ระยะเวลาสูงสุดที่ธุรกิจทนการหยุดชะงักได้ก่อนผลกระทบไม่ยอมรับ | โดยหลัก Recovery target ต้องไม่ช้ากว่าขีดจำกัดทางธุรกิจ และนิยามต้องตรงกันในองค์กร |
| **Hot/Warm/Cold Site** | สถานที่สำรองที่มีความพร้อมต่างระดับ จากพร้อมมากไปเตรียมน้อย | ความพร้อมจริง ค่าใช้จ่าย ข้อมูล อุปกรณ์ คน และเวลาทดสอบ เทียบ RTO/RPO |
| **Tabletop Exercise** | การซ้อมโดยอภิปรายตามสถานการณ์ ไม่ได้กู้ระบบจริงทั้งหมด | ใช้ทดสอบบทบาทและการตัดสินใจ แต่ไม่ควรอ้างเป็นหลักฐานว่าระบบกู้ได้ภายในเวลาจริง |
| **DR Drill/Recovery Test** | การทดสอบการกู้คืนด้วยขั้นตอนและระบบตามขอบเขต | Scope, scenario, start/end timestamp, data validation, issue, rollback และ retest |
| **Resilience** | ความสามารถเตรียม รับมือ ฟื้นตัว และปรับตัวจากเหตุขัดข้อง | มองเกิน Redundancy ไปถึงคน กระบวนการ Supplier การเรียนรู้ และการตัดสินใจ |

## 9. Cloud, Outsourcing และบริการจากภายนอก

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Cloud Computing** | การใช้ทรัพยากร IT ผ่านผู้ให้บริการและบริหารผ่านระบบเครือข่าย | Shared responsibility, region, access, configuration, logging, backup, vendor และ exit |
| **IaaS** | ผู้ให้บริการจัดโครงสร้างพื้นฐาน ส่วนลูกค้าดูแล OS/Application มากขึ้น | แยกให้ชัดว่าใคร Patch/Configure/Monitor แต่ละ Layer |
| **PaaS** | ผู้ให้บริการดูแล Platform มากขึ้น ลูกค้าพัฒนา/ตั้งค่า Application และข้อมูล | Access, secure configuration, code, data และ interface ยังเป็นความรับผิดชอบลูกค้า |
| **SaaS** | ใช้ Application สำเร็จรูปผ่านบริการ เช่น Email หรือ CRM | User/role, configuration, data export, log, retention, integration และ vendor assurance |
| **Shared Responsibility Model** | การแบ่งความรับผิดชอบระหว่างผู้ให้บริการกับลูกค้า | ต้อง Mapping Control รายข้อ ไม่ใช้คำว่า “อยู่บน Cloud จึงเป็นหน้าที่ Vendor” |
| **Cloud Region/Availability Zone** | พื้นที่และกลุ่มศูนย์ข้อมูลที่แยกกันตามการออกแบบผู้ให้บริการ | Data location, redundancy และการกระจายระบบแยก Failure domain จริงหรือไม่ |
| **Third Party/Vendor** | บุคคลหรือองค์กรภายนอกที่ให้สินค้า บริการ หรือเข้าถึงระบบ/ข้อมูล | Inventory, risk tier, due diligence, contract, access, monitoring, incident และ termination |
| **Outsourcing** | การให้ภายนอกดำเนินกิจกรรมแทนองค์กร | ความรับผิดชอบสุดท้ายยังต้องกำกับดูแล กำหนด SLA, control, evidence และ exit plan |
| **SOC Report** | รายงานให้ความเชื่อมั่นเกี่ยวกับ Control ของ Service Organization ตามขอบเขตที่ระบุ | ดูชนิด Scope, period, auditor opinion, exception, subservice และ CUECs ไม่ดูเพียงหน้าปก |
| **SOC 1** | รายงาน Control ที่เกี่ยวข้องกับการรายงานทางการเงินของผู้ใช้บริการ | ใช้เมื่อบริการกระทบ Financial reporting และต้อง Mapping control objective กับความเสี่ยงองค์กร |
| **SOC 2** | รายงาน Control ตาม Trust Services Criteria เช่น Security และ Availability ตาม Scope | ดูว่าครอบคลุม Criteria/บริการ/สถานที่/ช่วงเวลาที่ต้องการจริงหรือไม่ |
| **Type 1** | ประเมิน Description และการออกแบบ Control ณ วันที่กำหนด | ไม่พิสูจน์ว่า Control ทำงานตลอดช่วงเวลา |
| **Type 2** | ประเมิน Description, Design และ Operating Effectiveness ตลอดช่วงที่กำหนด | อ่านผลทดสอบและข้อยกเว้น รวมช่วงเวลาที่ไม่ครอบคลุม |
| **CUEC (Complementary User Entity Control)** | Control ที่ลูกค้าต้องทำเองเพื่อให้ Control ของผู้ให้บริการบรรลุผล | กระทบยอด CUEC กับ Owner/Control/หลักฐานขององค์กร ห้ามถือว่า SOC ครอบคลุมทุกอย่าง |
| **SLA** | ข้อตกลงระดับบริการกับผู้ให้บริการ | นิยามเวลา วัดจากแหล่งใด exclusion/service credit และการติดตาม breach |
| **Exit Plan** | แผนย้ายออกหรือเลิกใช้ผู้ให้บริการ | คืน/ย้ายข้อมูล ลบสำเนา เปลี่ยน Interface ยกเลิกสิทธิ์ และทดสอบความเป็นไปได้ |

## 10. การพัฒนา การเปลี่ยนแปลง และ DevOps

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **SDLC (System/Software Development Life Cycle)** | วงจรตั้งแต่ต้องการ ออกแบบ พัฒนา ทดสอบ ใช้งาน และบำรุงรักษาระบบ | Security/Control requirement, approval, traceability, test และ segregation ตลอดวงจร |
| **Agile** | วิธีพัฒนาแบบรอบสั้นและส่งมอบเป็นส่วนๆ | Control ต้องฝังในแต่ละรอบ ไม่สรุปว่า Agile ไม่ต้องมีเอกสารหรืออนุมัติ |
| **Waterfall** | วิธีพัฒนาเป็นขั้นต่อเนื่องตามลำดับ | การเปลี่ยน Requirement, stage approval, testing และความเสี่ยงพบปัญหาช้า |
| **DevOps** | แนวทางร่วมมือและทำ Automation ระหว่าง Development กับ Operations | Pipeline access, change approval, automated test, secret และ deployment evidence |
| **DevSecOps** | ฝัง Security เข้าใน DevOps และ SDLC | Security test เป็น Gate จริงหรือเพียงรายงาน ใครจัดการข้อยกเว้นและ false positive |
| **Repository** | พื้นที่เก็บ Source Code และประวัติ Version เช่น Git repository | Access, branch protection, review, commit identity, secret scanning และ backup |
| **CI/CD Pipeline** | กระบวนการอัตโนมัติ Build, Test และ Deploy ระบบ | ใครแก้ Pipeline/Approve Deploy ได้ Artifact integrity, segregation และ log |
| **Code Review** | การให้ผู้อื่นตรวจ Source Code ก่อนรวม/นำใช้ | Reviewer เป็นอิสระและมีทักษะ Scope ชัด และข้อคิดเห็นสำคัญถูกแก้หรือไม่ |
| **SAST** | วิเคราะห์ Source/byte code เพื่อหาจุดอ่อนโดยไม่รันระบบจริง | Scope, rule, severity, false positive, exception และแก้ก่อน Release |
| **DAST** | ทดสอบ Application ที่กำลังรันจากภายนอกเพื่อหาจุดอ่อน | Environment, authentication coverage, API coverage, impact และ remediation |
| **Software Composition Analysis (SCA)** | ตรวจ Library/Dependency ภายนอกและช่องโหว่/License | Inventory/SBOM, version, transitive dependency, patch และ accepted risk |
| **SBOM (Software Bill of Materials)** | รายการส่วนประกอบซอฟต์แวร์และ Version | สร้าง/อัปเดตครบหรือไม่ เชื่อมช่องโหว่กับระบบที่ใช้งานจริงได้หรือไม่ |
| **Deployment** | การนำ Code/Configuration ไปติดตั้งใน Environment | Approved artifact, operator, timestamp, automated/manual step, rollback และ verification |
| **Rollback/Backout Plan** | แผนย้อนกลับหากการเปลี่ยนล้มเหลว | ทำได้จริง ข้อมูลที่เปลี่ยนย้อนอย่างไร และผ่านการทดสอบหรือไม่ |
| **Emergency Change** | การเปลี่ยนเร่งด่วนเพื่อแก้เหตุสำคัญ | เกณฑ์ฉุกเฉิน อนุมัติเท่าที่ทำได้ Log, testing, retrospective approval และ post-review |
| **Technical Debt** | งานปรับปรุงเทคนิคที่ถูกเลื่อนและสะสม | เชื่อมกับ Stability, supportability และ Risk ไม่ใช้เป็นเหตุผลเลื่อน Control โดยไม่มี Owner/แผน |
| **Security Debt** | ช่องโหว่ Finding ข้อยกเว้น และ Control gap ที่สะสมจากการเลื่อนจัดการ | Severity, อายุ, การเกิดซ้ำ, Owner, due date, risk acceptance และแนวโน้ม |

## 11. การตรวจสอบ ความเสี่ยง และหลักฐาน

| คำศัพท์ | ความหมายแบบง่าย | มุมที่ผู้ตรวจควรสนใจ |
|---|---|---|
| **Audit Universe** | รายการหน่วย ระบบ กระบวนการ และหัวข้อที่อาจถูกตรวจ | ครบและทันต่อการเปลี่ยนธุรกิจ/เทคโนโลยีหรือไม่ ใช้จัดแผนตามความเสี่ยง |
| **Audit Plan** | แผนว่าจะตรวจเรื่องใด เมื่อใด และใช้ทรัพยากรเท่าใด | เชื่อม Risk assessment, priority, skill และ coverage |
| **Audit Program** | รายละเอียดวัตถุประสงค์ Control และขั้นตอนตรวจของงานหนึ่ง | ผู้ตรวจอีกคนทำตามได้ เชื่อม Risk-Control-Test-Evidence และระบุ Population/period |
| **Scope** | ขอบเขตระบบ กระบวนการ สถานที่ ช่วงเวลา และสิ่งที่รวม/ไม่รวม | Scope ต้องพอให้ตอบวัตถุประสงค์ และข้อจำกัดต้องปรากฏในข้อสรุป |
| **Criteria** | เกณฑ์สำหรับเปรียบเทียบสิ่งที่พบ | ใช้ Policy, กฎหมาย สัญญา มาตรฐาน หรือค่าที่อนุมัติซึ่งใช้กับองค์กรและช่วงเวลาจริง |
| **Inherent Risk** | ความเสี่ยงก่อนพิจารณา Control | ประเมินตามธรรมชาติของกิจกรรม Exposure และผลกระทบ ไม่ลดคะแนนเพราะมี Control แล้ว |
| **Residual Risk** | ความเสี่ยงที่เหลือหลังพิจารณา Control | ต้องอิงประสิทธิผลของ Control และเทียบ Risk appetite/tolerance |
| **Risk Appetite** | ระดับ/ประเภทความเสี่ยงที่องค์กรยอมรับเพื่อบรรลุเป้าหมาย | ผู้มีอำนาจอนุมัติ สื่อสารไปสู่เกณฑ์ปฏิบัติ และใช้ตัดสินใจจริงหรือไม่ |
| **Risk Tolerance** | ขอบเขตความเบี่ยงเบนหรือระดับยอมรับในเรื่องเฉพาะ | นิยามวัดได้และสอดคล้อง Appetite เช่น RTO หรือ Threshold |
| **Control** | การกระทำหรือกลไกที่จัดการความเสี่ยง | ใครทำอะไร เมื่อใด ด้วยข้อมูล/ระบบใด และเหลือหลักฐานอะไร |
| **Preventive Control** | ป้องกันก่อนปัญหาเกิด | เช่น บล็อกสิทธิ์หรือบังคับอนุมัติ ต้องทดสอบว่าข้ามได้หรือไม่ |
| **Detective Control** | ตรวจพบปัญหาที่เกิดแล้ว | ต้องมีคนตรวจตามรอบ เกณฑ์ชัด และติดตามผล ไม่ใช่เพียงสร้าง Report |
| **Corrective Control** | แก้ไขหรือฟื้นฟูหลังพบปัญหา | แก้ผลและต้นเหตุ มี Owner/เวลา และตรวจประสิทธิผลหลังแก้ |
| **Manual Control** | บุคคลเป็นผู้ดำเนิน Control | ความรู้ ความสม่ำเสมอ หลักฐาน Reviewer และความเสี่ยง Human error |
| **Automated Control** | ระบบดำเนิน Control ตาม Logic/Configuration | พึ่งพา Access/Change/Operations ITGC และต้องตรวจ Logic/Configuration |
| **IT-Dependent Manual Control** | บุคคลตรวจโดยพึ่งรายงานหรือข้อมูลจากระบบ | ต้องตรวจทั้งการ Review ของคนและความครบ/ถูกของรายงานหรือ IPE |
| **Key Control** | Control สำคัญที่หากล้มเหลวมีผลต่อความเสี่ยง/วัตถุประสงค์มาก | เหตุผลที่เป็น Key, dependency และระดับการทดสอบ |
| **Compensating Control** | Control อื่นที่ลดความเสี่ยงแทน Control หลักที่ขาด | ต้องจัดการความเสี่ยงเดียวกัน ทันเวลา และทดสอบประสิทธิผล ไม่ใช่เพียง Control ที่เกี่ยวข้อง |
| **Test of Design** | ประเมินว่าหากทำตามที่ออกแบบจะจัดการความเสี่ยงได้หรือไม่ | ดู Risk coverage, owner, frequency, precision, evidence และ exception handling |
| **Test of Implementation** | ประเมินว่า Control ถูกนำไปใช้จริง | Walkthrough/ตัวอย่างช่วยยืนยันการมีอยู่ แต่ยังไม่สรุปทั้งช่วง |
| **Operating Effectiveness** | ประเมินว่า Control ทำงานตามแบบอย่างสม่ำเสมอตลอดช่วงที่ตรวจ | ต้องกำหนด Population, period, sample/data test และประเมิน exception |
| **Walkthrough** | ติดตามรายการหนึ่งผ่านกระบวนการเพื่อเข้าใจคน ระบบ Control และหลักฐาน | ใช้ยืนยันความเข้าใจและ implementation ไม่แทนการทดสอบทั้งปีโดยอัตโนมัติ |
| **Inquiry** | การสอบถามผู้รู้หรือผู้ปฏิบัติงาน | ใช้มากแต่หลักฐานมีน้ำหนักจำกัด ควร Corroborate ด้วยเอกสาร ข้อมูล หรือการสังเกต |
| **Observation** | การสังเกตการทำงานหรือสภาพจริง | พิสูจน์ ณ เวลาที่เห็น และคนอาจทำต่างเมื่อรู้ว่าถูกสังเกต |
| **Inspection** | การตรวจเอกสาร Record Configuration หรือทรัพย์สิน | ประเมินแหล่งที่มา ความแท้ ความครบ และสิ่งที่เอกสารพิสูจน์ได้จริง |
| **Recalculation** | คำนวณซ้ำเพื่อตรวจความถูกต้องเชิงคณิตศาสตร์ | ใช้กฎ/อัตราที่อนุมัติและจัดการการปัดเศษ/Boundary ชัด |
| **Reperformance** | ผู้ตรวจทำขั้นตอนหรือ Control ซ้ำอย่างอิสระ | ให้หลักฐานตรง แต่ต้องคำนึงถึงสิทธิ์ ผลกระทบ และ Environment |
| **System Query** | ดึงหรือทดสอบข้อมูลโดยใช้คำสั่งต่อระบบ | ผู้ทำต้องมีความรู้ ได้รับอนุญาต ใช้ Read-only เมื่อเหมาะสม และบันทึก Query/parameter |
| **CAATs** | เทคนิคใช้คอมพิวเตอร์ช่วยตรวจ เช่น วิเคราะห์ข้อมูลหรือ Test Data | Data reliability, repeatability, exception และการเก็บ Script/ผลลัพธ์ |
| **Population** | รายการทั้งหมดที่อยู่ในขอบเขตการทดสอบ | ตรวจความครบถ้วน ช่วงเวลา แหล่งและ Filter ก่อนเลือก Sample |
| **Sample** | รายการบางส่วนที่เลือกจาก Population | วิธีเลือกและขนาดต้องเหมาะกับวัตถุประสงค์ ความถี่ Control และความเสี่ยง |
| **Evidence** | ข้อมูลที่รองรับสิ่งที่ผู้ตรวจทำและสรุป | ต้องเพียงพอ น่าเชื่อถือ เกี่ยวข้อง ทันเวลา และตรวจย้อนกลับได้ |
| **IPE (Information Produced by the Entity)** | รายงานหรือข้อมูลที่องค์กรสร้างและใช้เป็นหลักฐาน/Control | ตรวจ Source, logic, parameter, completeness, accuracy และ change control |
| **Working Paper** | บันทึกวัตถุประสงค์ วิธีตรวจ หลักฐาน ผล และข้อสรุป | Reviewer ต้องตามได้ว่าใครทำอะไร ข้อมูลใด ช่วงใด และสรุปได้อย่างไร |
| **Finding/Observation** | เรื่องที่ผู้ตรวจพบและเห็นว่าควรสื่อสาร | มี Criteria, Condition, Cause, Effect/Risk และ Action ที่มีหลักฐานรองรับ |
| **Exception** | รายการที่ไม่เป็นไปตามเกณฑ์หรือผลคาดหวัง | ต้องหาสาเหตุ ขอบเขต และผลกระทบ ไม่สรุปว่า Control ล้มเหลวทั้งหมดหรือเป็นเรื่องเล็กก่อนวิเคราะห์ |
| **Root Cause** | สาเหตุพื้นฐานที่ทำให้ปัญหาเกิดหรือเกิดซ้ำ | ต้องพิสูจน์ ไม่คาดเดา และแยกจากอาการ เช่น “พนักงานผิดพลาด” อาจยังไม่ใช่ Root cause |
| **Recommendation** | ข้อเสนอของผู้ตรวจเพื่อจัดการความเสี่ยง/สาเหตุ | ระบุผลลัพธ์ที่ต้องการโดยไม่ออกแบบงานแทน Management เกินจำเป็น |
| **Management Action Plan** | แผนที่ผู้บริหารรับผิดชอบดำเนินการแก้ไข | Action, owner, due date, dependency และหลักฐานปิดประเด็นชัด |
| **Follow-up/Retest** | การตรวจว่าการแก้ไขทำเสร็จและได้ผล | ไม่ปิดจากคำยืนยันหรือเอกสารแผนเพียงอย่างเดียว ต้องทดสอบตามความเสี่ยง |

## 12. คำย่อและคำที่มักสับสน

| คู่คำ | ความต่างที่ควรจำ |
|---|---|
| **Internet / Intranet / Extranet** | Internet คือเครือข่ายสาธารณะ; Intranet ใช้ภายในองค์กร; Extranet เปิดพื้นที่จำกัดให้บุคคลภายนอกที่ได้รับอนุญาต |
| **API / Interface / Integration** | API เป็นวิธีหนึ่งที่ระบบเปิดให้เรียกใช้; Interface คือจุด/กลไกแลกข้อมูลทุกแบบ; Integration คือภาพรวมการทำให้ระบบทำงานร่วมกัน |
| **Authentication / Authorization** | Authentication พิสูจน์ว่าเป็นใคร; Authorization กำหนดว่าทำอะไรได้ |
| **Event / Log / Alert / Incident** | Event คือสิ่งที่เกิด; Log คือบันทึก; Alert คือการแจ้งตามเงื่อนไข; Incident คือเหตุที่ต้องจัดการเพราะมีหรืออาจมีผลกระทบ |
| **Backup / Snapshot / DR** | Backup คือสำเนาข้อมูล; Snapshot คือภาพสถานะ ณ เวลาและอาจอยู่ที่เดียวกับระบบ; DR คือความสามารถและกระบวนการกู้ระบบโดยรวม |
| **RTO / RPO** | RTO วัดเวลาที่ต้องฟื้นบริการ; RPO วัดจุดข้อมูลย้อนหลังที่ยอมสูญเสีย |
| **UPS / Generator** | UPS จ่ายไฟทันทีช่วงสั้นและช่วยรอ Generator/ปิดระบบ; Generator รองรับเหตุไฟดับนานกว่าแต่ต้องใช้เวลาเริ่มทำงาน |
| **Firewall / WAF** | Firewall ควบคุม Traffic เครือข่ายทั่วไป; WAF วิเคราะห์คำขอ Web/Application โดยเฉพาะ |
| **IDS / IPS** | IDS เน้นตรวจจับและแจ้ง; IPS สามารถบล็อกตาม Rule |
| **VA / PT** | VA เน้นค้นหา/ประเมินช่องโหว่; PT พยายามพิสูจน์การใช้ประโยชน์ภายใต้ขอบเขตและกติกา |
| **Encryption / Hashing / Masking** | Encryption ถอดกลับได้ด้วย Key; Hash โดยทั่วไปใช้ตรวจ/เปรียบเทียบและไม่ถอดกลับ; Masking ซ่อนบางส่วนเพื่อจำกัดการมองเห็น |
| **ITGC / Application Control** | ITGC เป็นพื้นฐานข้ามระบบ; Application Control จัดการรายการ/ข้อมูลในกระบวนการเฉพาะ และมักพึ่ง ITGC |
| **Design / Implementation / Operating Effectiveness** | ออกแบบเหมาะหรือไม่; นำมาใช้จริงหรือไม่; ทำงานสม่ำเสมอตลอดช่วงหรือไม่ |
| **Finding / Vulnerability / Incident** | Finding คือผลจากการตรวจ; Vulnerability คือจุดอ่อน; Incident คือเหตุการณ์ที่เกิดหรือสงสัยว่ากระทบจริง คำหนึ่งไม่แปลว่าอีกคำเกิดขึ้นแล้ว |
| **Risk / Issue** | Risk มองความไม่แน่นอนที่อาจเกิด; Issue คือปัญหาหรือสภาพที่เกิด/มีอยู่แล้ว แม้หลายองค์กรจะใช้คำต่างกัน |
| **SOC (Security Operations Center) / SOC Report** | SOC แบบแรกคือทีมเฝ้าระวังภัย; SOC Report คือรายงานให้ความเชื่อมั่นของ Service Organization ต้องดูบริบททุกครั้ง |

## 13. ประโยคถามกลับเมื่อได้ยินศัพท์ที่ไม่คุ้น

ใช้คำถามต่อไปนี้แทนการรีบตอบว่าเข้าใจ:

1. ในองค์กรนี้คำนี้หมายถึงผลิตภัณฑ์ กระบวนการ ทีม หรือ Control อะไร?
2. อยู่ในระบบ Production, Test, On-premises หรือ Cloud และใครเป็น Owner?
3. ครอบคลุม Application, Server, User หรือข้อมูลใดบ้าง และรู้ได้อย่างไรว่ารายการครบ?
4. ความเสี่ยงที่สิ่งนี้ตั้งใจจัดการคือเหตุการณ์และผลกระทบอะไร?
5. ค่า Policy/Configuration/Threshold ใครอนุมัติ และเปลี่ยนล่าสุดเมื่อใด?
6. หาก Control ทำงานหรือไม่ทำงาน จะเหลือ Log, Ticket, Report หรือหลักฐานใด?
7. มีข้อยกเว้น ระบบเก่า หรือพื้นที่ที่ยังไม่ครอบคลุมหรือไม่?
8. มีการทดสอบ Failover, Restore, Detection หรือขั้นตอนตอบสนองจริงครั้งล่าสุดเมื่อใด และผลเป็นอย่างไร?

## เอกสารที่เกี่ยวข้อง

- [ภาพรวมงาน IT Audit และตาราง Risk-Control-Test-Evidence](</Users/sarayutpanlom/Library/CloudStorage/OneDrive-Personal/Codex/IT_Audit/output/IT_Audit_Overview_Map_TH.md>)
- [คู่มือ IT Audit ตั้งแต่พื้นฐาน](</Users/sarayutpanlom/Library/CloudStorage/OneDrive-Personal/Codex/IT_Audit/output/IT_Audit_Foundation_Teaching_Guide_TH.md>)
- [บทเสริมจากเอกสาร ISACA](</Users/sarayutpanlom/Library/CloudStorage/OneDrive-Personal/Codex/IT_Audit/output/ISACA_Teaching_Supplement_TH.md>)
- [ดัชนีเอกสารทั้งหมด](</Users/sarayutpanlom/Library/CloudStorage/OneDrive-Personal/Codex/IT_Audit/output/IT_Audit_File_Index_TH.md>)
