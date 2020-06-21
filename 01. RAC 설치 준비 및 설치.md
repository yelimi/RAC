#  RAC 설치 준비 및 설치
-------------------------------------------

* 1) 가상 시스템 생성
	* ![1](https://user-images.githubusercontent.com/58458582/84667815-d0e96f00-af5d-11ea-8905-854ff7304989.PNG)
	* ![2](https://user-images.githubusercontent.com/58458582/84667819-d2b33280-af5d-11ea-94ee-9f4bc5b7ef8a.PNG)
	* ![3](https://user-images.githubusercontent.com/58458582/84667822-d34bc900-af5d-11ea-9147-5065c7ff53df.PNG)
	* ![4](https://user-images.githubusercontent.com/58458582/84667824-d3e45f80-af5d-11ea-8fd1-75e13ef97b6d.PNG)
	* ![5](https://user-images.githubusercontent.com/58458582/84667825-d3e45f80-af5d-11ea-83b5-de902c21bb2f.PNG)
	* ![6](https://user-images.githubusercontent.com/58458582/84667827-d47cf600-af5d-11ea-893a-33120162d178.PNG)
	* ![7](https://user-images.githubusercontent.com/58458582/84667829-d5158c80-af5d-11ea-81e5-35fecdc48381.PNG)
	* ![8](https://user-images.githubusercontent.com/58458582/84667830-d5158c80-af5d-11ea-86e0-e2d565cd7dcf.PNG)
	* ![9](https://user-images.githubusercontent.com/58458582/84667831-d5ae2300-af5d-11ea-8b6b-9965466dd24c.PNG)
	* ![10](https://user-images.githubusercontent.com/58458582/84667833-d5ae2300-af5d-11ea-84fa-d98c25324570.PNG)
	* ![11](https://user-images.githubusercontent.com/58458582/84667836-d646b980-af5d-11ea-88de-2a9684b85542.PNG)
	* ![12](https://user-images.githubusercontent.com/58458582/84667840-d6df5000-af5d-11ea-84dc-b02e92a3056d.PNG)
		* -> local disk 500GB이상 생성
	*  
	* // edit virtual machine settings
	* ![13](https://user-images.githubusercontent.com/58458582/84667841-d777e680-af5d-11ea-86c1-9ecc90fbcc91.PNG)
	* ![14](https://user-images.githubusercontent.com/58458582/84667847-d8a91380-af5d-11ea-882b-d152b13277c5.PNG)
		* host-only로 추가
	* ![14-1](https://user-images.githubusercontent.com/58458582/84667843-d8107d00-af5d-11ea-994e-6a39116d4dbf.PNG)
		* mac address 맨뒤만 기억(4D)
	* ![14-2](https://user-images.githubusercontent.com/58458582/84667844-d8107d00-af5d-11ea-91f0-a3759772f119.PNG)
		* mac address 맨뒤만 기억(D1)
	*  
	* ![15](https://user-images.githubusercontent.com/58458582/84667848-d8a91380-af5d-11ea-843c-3ea48f2c4da7.PNG)
	* ![16](https://user-images.githubusercontent.com/58458582/84667850-d941aa00-af5d-11ea-8aac-8b2f65dabeea.PNG)
	* ![17](https://user-images.githubusercontent.com/58458582/84667853-d9da4080-af5d-11ea-9878-2c6066e4d274.PNG)
	* ![18](https://user-images.githubusercontent.com/58458582/84667855-d9da4080-af5d-11ea-9d59-5e2ae275381a.PNG)
	* ![19](https://user-images.githubusercontent.com/58458582/84667857-da72d700-af5d-11ea-86ab-7f021db5041d.PNG)
	* ![20](https://user-images.githubusercontent.com/58458582/84667858-da72d700-af5d-11ea-9717-ebd0eb010cf4.PNG)
		* -> 똑같은 방법으로 shared disk 5개 이상 생성
		* -> 각각에 대해 SCSI 1:0~4 설정
	*  
	* ![21 rac11g TO shared 이동](https://user-images.githubusercontent.com/58458582/84667861-db0b6d80-af5d-11ea-9c4e-46fc1bdfa7f7.PNG)
		* Shared 폴더로 이동
	*  
	* C:\Image\RAC11g\RAC1\RAC1.vmx 편집 
	* 추가
	* ![22 추가](https://user-images.githubusercontent.com/58458582/84667863-dba40400-af5d-11ea-9946-9a102947a023.PNG)
	* ![23 추가](https://user-images.githubusercontent.com/58458582/84667865-dba40400-af5d-11ea-9435-5b05dc0c9358.PNG)
	* ![24 추가](https://user-images.githubusercontent.com/58458582/84667867-dc3c9a80-af5d-11ea-835e-aab93d99fb5b.PNG)
	*  
	* ![25 결과 확인](https://user-images.githubusercontent.com/58458582/84667868-dc3c9a80-af5d-11ea-9275-11e2d44cd9c0.PNG)
		* 가상 시스템 생성 결과 확인
* 2) 리눅스 설치
	* ![26 LVM 등 삭제](https://user-images.githubusercontent.com/58458582/84667869-dcd53100-af5d-11ea-9d78-3a749b8ff05f.PNG)
		* LVM 등 삭제
	* ![27](https://user-images.githubusercontent.com/58458582/84667874-dcd53100-af5d-11ea-87ce-8b78e9ac899a.PNG)
	* ![28](https://user-images.githubusercontent.com/58458582/84667875-dd6dc780-af5d-11ea-91c5-154db9909e5a.PNG)
	* ![29 4d 일치 확인](https://user-images.githubusercontent.com/58458582/84667876-de065e00-af5d-11ea-92d5-8213dd76e573.PNG)
		* 맥주소 맨뒤(4D, D1) 일치하는지 확인
	* ![30](https://user-images.githubusercontent.com/58458582/84667878-de9ef480-af5d-11ea-861e-ae8fe4a5d917.PNG)
	* ![31](https://user-images.githubusercontent.com/58458582/84667880-de9ef480-af5d-11ea-8d07-1879e2bcc8e5.PNG)
	* ![32](https://user-images.githubusercontent.com/58458582/84667882-df378b00-af5d-11ea-8979-da0b72f9860e.PNG)
	* ![33](https://user-images.githubusercontent.com/58458582/84667883-df378b00-af5d-11ea-9d3c-097f12709763.PNG)
	* 설치 옵션
	* <img width="353" alt="34" src="https://user-images.githubusercontent.com/58458582/84669734-2aeb3400-af60-11ea-8bab-2ea42d4b8e30.png">
	*  
	* // VMware Tools 설치
	*  
	* // group, user 생성 및 준비
	* [root@host01 ~]# userdel oracle
	* [root@host01 ~]# userdel grid
	* [root@host01 ~]# groupdel oinstall
	* [root@host01 ~]# groupdel dba
	*  
	* [root@host01 ~]# rm -rf /home/oracle
	* [root@host01 ~]# rm -rf /home/grid
	*  
	* [root@host01 ~]# groupadd dba
	* [root@host01 ~]# groupadd oinstall
	* [root@host01 ~]# groupadd oper
	* [root@host01 ~]# groupadd asmadmin
	* [root@host01 ~]# groupadd asmdba
	* [root@host01 ~]# groupadd asmoper
	*  
	* [root@host01 ~]# useradd -g oinstall -G asmoper,asmdba,asmadmin grid
	* [root@host01 ~]# useradd -g oinstall -G dba,oper,asmdba oracle
	*  
	* [root@host01 ~]# passwd oracle --stdin << ENDPWD
	* oracle
	* oracle
	* ENDPWD
	*  
	* [root@host01 ~]# passwd grid --stdin << ENDPWD
	* oracle
	* oracle
	* ENDPWD
	*  
	* [root@host01 ~]# vi /home/oracle/.bash_profile
	* 추가
	* ![00](https://user-images.githubusercontent.com/58458582/84669841-4bb38980-af60-11ea-86c1-911098824eff.PNG)
	*  
	* [root@host01 ~]# vi /home/grid/.bash_profile
	* 추가
	* ![01](https://user-images.githubusercontent.com/58458582/84669845-4ce4b680-af60-11ea-85b6-8703034bbe03.PNG)
	*  
	* [root@host01 ~]# vi /root/.bash_profile
	* 추가
	* ![02](https://user-images.githubusercontent.com/58458582/84669854-4e15e380-af60-11ea-9c5b-59ba19900452.PNG)
	*  
	* // 기본  패키지 설치
	* virtual machine setting - device status 체크 - use ISO image file 설정 ( -> cd 넣기)
	*  
	* ![03](https://user-images.githubusercontent.com/58458582/84669862-50783d80-af60-11ea-973b-993ef871fb8f.PNG)
	*  
	* // 추가 패키지 설치
	* virtual machine settings - shared folders - always enabled 체크 - share 폴더 추가
	*  
	* ![04](https://user-images.githubusercontent.com/58458582/84669871-52da9780-af60-11ea-80cd-d764d263e49f.PNG)
	*  
	* // 시스템 설정
	* [root@host01 ~]# vi /etc/sysctl.conf
	* 추가
	* ![05](https://user-images.githubusercontent.com/58458582/84669874-540bc480-af60-11ea-9b34-fce7f76e9d78.PNG)
	*  
	* [root@host01 ~]# vi /etc/security/limits.conf
	* 추가
	* ![06](https://user-images.githubusercontent.com/58458582/84669878-553cf180-af60-11ea-8468-3922605f8d15.PNG)
	*  
	* [root@host01 ~]# vi /etc/pam.d/login
	* 추가
	* session    required     pam_limits.so
	*  
	* [root@host01 ~]# vi /etc/hosts
	* 추가
	* ![07](https://user-images.githubusercontent.com/58458582/84669882-55d58800-af60-11ea-8a35-e7c1e7161d3f.PNG)
	*  
	* [root@host01 ~]# vi /etc/sysconfig/ntpd
	* 수정
	* OPTIONS="-x -u ntp:ntp -p /var/run/ntpd.pid"
	*  
	* [root@host01 ~]# service ntpd stop
	* [root@host01 ~]# chkconfig ntpd off
	*  
	* [root@host01 ~]# service nscd start
	* [root@host01 ~]# chkconfig nscd on 
	*   
	* [root@host01 ~]# service iptables stop
	* [root@host01 ~]# chkconfig iptables off
	*  
	* [root@host01 ~]# service sendmail stop
	* [root@host01 ~]# chkconfig sendmail off
	*  
	* [root@host01 ~]# getenforce disabled
	*  
	* // 설치 경로 준비
	* [root@host01 ~]# mkdir -p /u01/app/grid
	* [root@host01 ~]# mkdir -p /u01/app/11.2.0.3/grid
	* [root@host01 ~]# chown -R grid:oinstall /u01/app
	* [root@host01 ~]# chmod -R 775 /u01/app/grid
	* [root@host01 ~]# chmod -R 775 /u01/app/11.2.0.3/grid
	* [root@host01 ~]# mkdir -p /u01/app/oracle
	* [root@host01 ~]# chown -R oracle:oinstall /u01/app/oracle
	*   
	* // 디스크 준비
	* [root@host01 ~]# fdisk -l
	*  
	* [root@host01 ~]# fdisk /dev/sdb
	* ![디스크준비](https://user-images.githubusercontent.com/58458582/84669896-5a01a580-af60-11ea-8bf1-8ca620ec8a12.PNG)
	* [root@host01 ~]# fdisk /dev/sdc
		* 위와 동일한 방법으로
	* [root@host01 ~]# fdisk /dev/sdd
		* 위와 동일한 방법으로
	* [root@host01 ~]# fdisk /dev/sde
		* 위와 동일한 방법으로
	* [root@host01 ~]# fdisk /dev/sdf
		* 위와 동일한 방법으로
	*  
	* // ASM DISK 준비
	* [root@host01 ~]# oracleasm configure -i
	* ![asm disk 준비](https://user-images.githubusercontent.com/58458582/84669899-5b32d280-af60-11ea-8847-9d4eed2d56cd.PNG)
	*  
	* [root@host01 ~]# oracleasm exit
	* [root@host01 ~]# oracleasm init
	*  
	* [root@host01 ~]# oracleasm createdisk ASMDISK01 /dev/sdb1
	* [root@host01 ~]# oracleasm createdisk ASMDISK02 /dev/sdc1
	* [root@host01 ~]# oracleasm createdisk ASMDISK03 /dev/sdd1
	* [root@host01 ~]# oracleasm createdisk ASMDISK04 /dev/sde1
	* [root@host01 ~]# oracleasm createdisk ASMDISK05 /dev/sdf1
	*  
	* [root@host01 ~]# oracleasm scandisks
	* [root@host01 ~]# oracleasm listdisks
	* ![08](https://user-images.githubusercontent.com/58458582/84669885-566e1e80-af60-11ea-9dd9-8433d9651186.PNG)
	*  
	* [root@host01 ~]# shutdown -h now 
	*   
	* // VMware 종료 후 RAC1 이미지 복사 (=> RAC2)
	* rac2 실행시 copied it 선택
	*  
	* 여러 설정 후 리부팅
	* ![1 deactivate 클릭 inactive](https://user-images.githubusercontent.com/58458582/84670428-178c9880-af61-11ea-848c-c10c5d664177.PNG)
		* deactivate로 inactive
	* ![2 bak 삭제](https://user-images.githubusercontent.com/58458582/84670432-18252f00-af61-11ea-9bf2-063433412120.PNG)
		* bak delete
	* ![3 ip 설정](https://user-images.githubusercontent.com/58458582/84670434-19565c00-af61-11ea-86f8-a4231816ab1c.PNG)
		* ip 설정
	* ![4 ip 설정](https://user-images.githubusercontent.com/58458582/84670435-19eef280-af61-11ea-8ec1-0c167e4f6538.PNG)
		* ip 설정
	* ![5 dns 설정](https://user-images.githubusercontent.com/58458582/84670437-1b201f80-af61-11ea-8d18-b47c1c9941ae.PNG)
		* dns 설정
	* ![6 active로 변경](https://user-images.githubusercontent.com/58458582/84670440-1bb8b600-af61-11ea-8e36-35c7e476ff26.PNG)
		* activate로 active
	*  
	* [root@host02 ~]# vi /etc/hosts
		*  host01 -> host02 로 수정
	* [root@host02 ~]# vi /home/oracle/.bash_profile
		* orcl1 -> orcl2 로 수정
	* [root@host02 ~]# vi /home/grid/.bash_profile
		* +ASM1 -> +ASM2 로 수정
	*  
	* [root@host01 ~]# oracleasm status
	* [root@host01 ~]# oracleasm listdisks
	*  
	* [root@host01 ~]# ping 192.168.100.111 -c 2
	* [root@host01 ~]# ping 192.168.100.112 -c 2
	* [root@host01 ~]# ping 192.168.200.111 -c 2
	* [root@host01 ~]# ping 192.168.200.112 -c 2
	* [root@host01 ~]# ping host01  -c 2
	* [root@host01 ~]# ping host02  -c 2
	* [root@host01 ~]# ping host01-priv  -c 2
	* [root@host01 ~]# ping host02-priv  -c 2
	* -> 잘 넘겨지나 확인
	*  
	* [root@host01 ~]# ssh host02
		* host02로 넘어감
	*  
	* [root@host02 ~]# oracleasm status
	* [root@host02 ~]# oracleasm listdisks
	*  
	* [root@host02 ~]# ping 192.168.100.111 -c 2
	* [root@host02 ~]# ping 192.168.100.112 -c 2
	* [root@host02 ~]# ping 192.168.200.111 -c 2
	* [root@host02 ~]# ping 192.168.200.112 -c 2
	* [root@host02 ~]# ping host01  -c 2
	* [root@host02 ~]# ping host02  -c 2
	* [root@host02 ~]# ping host01-priv  -c 2
	* [root@host02 ~]# ping host02-priv  -c 2
	*  
	* [root@host02 ~]# exit
	*  
	* [root@host01 ~]# mkdir /stage
	* [root@host01 ~]# cd /mnt/hgfs/share
	*  
	* [root@host01 share]# unzip  p10404530_112030_Linux-x86-64_1of7.zip -d /stage
	* [root@host01 share]# unzip  p10404530_112030_Linux-x86-64_2of7.zip -d /stage
	* [root@host01 share]# unzip  p10404530_112030_Linux-x86-64_3of7.zip -d /stage
	*  
	* [root@host01 share]# ssh host02 shutdown -h now
	*  
	* [root@host01 share]# shutdown -h now

