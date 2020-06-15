# GI, ASM, DB 설치
-------------

* 1) GI 설치
	* [+ASM1@host01 ~]$ cd /stage/grid
	* [+ASM1@host01 grid]$ ./runInstaller
	*  
	* ![gi 1](https://user-images.githubusercontent.com/58458582/84673807-25dcb380-af65-11ea-9a10-384c8a362045.PNG)
	* ![gi 2](https://user-images.githubusercontent.com/58458582/84673809-25dcb380-af65-11ea-9579-4a2cf6c85d32.PNG)
	* ![gi 3](https://user-images.githubusercontent.com/58458582/84673811-26754a00-af65-11ea-91ee-f0c6a6bd96f5.PNG)
	* ![gi 4 이름 변경](https://user-images.githubusercontent.com/58458582/84673813-26754a00-af65-11ea-8283-67a365aea789.PNG)
		* cluster 이름 변경
	* ![gi 5 host02 추가](https://user-images.githubusercontent.com/58458582/84673814-270de080-af65-11ea-9682-9e941db60c00.PNG)
		* host02 추가
	* ![gi 6-0 ssh 연결](https://user-images.githubusercontent.com/58458582/84673822-27a67700-af65-11ea-9c07-979c79483994.PNG)
		* ssh 연결
	* ![gi 6-1](https://user-images.githubusercontent.com/58458582/84673823-27a67700-af65-11ea-9775-30a82ad31190.PNG)
	* ![gi 7 확인](https://user-images.githubusercontent.com/58458582/84673827-283f0d80-af65-11ea-86c7-82ee4f5ede78.PNG)
	* ![gi 8 asm 선택](https://user-images.githubusercontent.com/58458582/84673829-28d7a400-af65-11ea-8f3b-cc7c4f1c7c7e.PNG)
		* ASM 선택
	* ![gi 9](https://user-images.githubusercontent.com/58458582/84673831-28d7a400-af65-11ea-814b-1d1f2de00902.PNG)
		* 디스크 그룹 생성, 디스크 선택
	* ![gi 10 pwd 설정](https://user-images.githubusercontent.com/58458582/84673833-29703a80-af65-11ea-9272-b96376fd92b6.PNG)
	* ![gi 11](https://user-images.githubusercontent.com/58458582/84673835-2a08d100-af65-11ea-9ea6-53e4d0c3f60a.PNG)
	* ![gi 12](https://user-images.githubusercontent.com/58458582/84673837-2a08d100-af65-11ea-8a75-6a7f7856922f.PNG)
	* ![gi 13](https://user-images.githubusercontent.com/58458582/84673841-2aa16780-af65-11ea-9a97-69b1c6931c34.PNG)
	* ![gi 14](https://user-images.githubusercontent.com/58458582/84673842-2b39fe00-af65-11ea-8484-ba6e74cb0cbc.PNG)
	* ![gi 15 ignore](https://user-images.githubusercontent.com/58458582/84673843-2b39fe00-af65-11ea-816d-51a234ba1cee.PNG)
		* 뭐가 걸리지만 ignore
	* ![gi 16 install](https://user-images.githubusercontent.com/58458582/84673844-2bd29480-af65-11ea-8c0c-f2d33db8b509.PNG)
	*  
	* [root@host01 ~]# /u01/app/oraInventory/orainstRoot.sh
	* [root@host01 ~]# ssh host02 /u01/app/oraInventory/orainstRoot.sh
	* [root@host01 ~]# /u01/app/11.2.0.3/grid/root.sh
	* [root@host01 ~]# ssh host02 /u01/app/11.2.0.3/grid/root.sh
* 2) ASMCA
	* ![asmca 1](https://user-images.githubusercontent.com/58458582/84673736-1198b680-af65-11ea-8854-7c2ff3f76c59.PNG)
		* 디스크 그룹 FRA 생성, 디스크 선택
	*  
	* [+ASM1@host01 ~]$ crsctl stat res -t
		* 정상적으로 설치됐는지 등.. 확인 작업
	* ![09](https://user-images.githubusercontent.com/58458582/84669894-58d07880-af60-11ea-854d-4db266012b51.PNG)
* 3) DB software install
	* [orcl1@host01 ~]$ cd /stage/database/
	*  
	* [orcl1@host01 database]$ id
	* (결과) uid=501(oracle) gid=501(oinstall) groups=500(dba),501(oinstall),502(oper),504(asmdba)
	*  
	* [orcl1@host01 database]$ ls
	* (결과) doc / readme.html  / rpm / sshsetup / welcome.html / install / response / runInstaller / stage
	*  
	* [orcl1@host01 database]$ ./runInstaller
	*  
	* ![db 1](https://user-images.githubusercontent.com/58458582/84673741-12c9e380-af65-11ea-9a77-76d25ff7b018.PNG)
	* ![db 2](https://user-images.githubusercontent.com/58458582/84673754-1a898800-af65-11ea-9bc1-2f4a050d6cf3.PNG)
	* ![db 3](https://user-images.githubusercontent.com/58458582/84673766-1d847880-af65-11ea-929f-723dead9725b.PNG)
	* ![db 4](https://user-images.githubusercontent.com/58458582/84673768-1eb5a580-af65-11ea-8f43-bcb459ff92aa.PNG)
		* ssh 연결
	* ![db 5](https://user-images.githubusercontent.com/58458582/84673770-1eb5a580-af65-11ea-8667-acdcd4838a3e.PNG)
	* ![db 6](https://user-images.githubusercontent.com/58458582/84673771-1f4e3c00-af65-11ea-9773-c1886cc3c308.PNG)
	* ![db 7](https://user-images.githubusercontent.com/58458582/84673772-1fe6d280-af65-11ea-954e-8a5a55adee12.PNG)
	* ![db 8 ignore](https://user-images.githubusercontent.com/58458582/84673774-1fe6d280-af65-11ea-944e-6a39697583d8.PNG)
		* 뭐가 걸리지만 ignore
	* ![db 9](https://user-images.githubusercontent.com/58458582/84673775-207f6900-af65-11ea-96b5-79c4a69395fe.PNG)
	*  
	* [root@host01 ~]# /u01/app/oracle/product/11.2.0.3/dbhome_1/root.sh
	* [root@host01 ~]# ssh host02 /u01/app/oracle/product/11.2.0.3/dbhome_1/root.sh
* 4) dbca
	* ![dbca 1](https://user-images.githubusercontent.com/58458582/84673779-207f6900-af65-11ea-9f41-6f39cabe83f8.PNG)
	* ![dbca 2](https://user-images.githubusercontent.com/58458582/84673781-2117ff80-af65-11ea-8580-e4383fe2be9b.PNG)
	* ![dbca 3](https://user-images.githubusercontent.com/58458582/84673783-21b09600-af65-11ea-8b6a-41d733bb9e7a.PNG)
	* ![dbca 4 selectall  orcl](https://user-images.githubusercontent.com/58458582/84673786-21b09600-af65-11ea-8906-9a383e9d5c3a.PNG)
		* orcl 설정, host 모두 select all
	* ![dbca 5](https://user-images.githubusercontent.com/58458582/84673791-22492c80-af65-11ea-9000-a03f2211bfe2.PNG)
	* ![dbca 6](https://user-images.githubusercontent.com/58458582/84673793-22e1c300-af65-11ea-83cd-bc49f25d4dde.PNG)
	* ![dbca 7](https://user-images.githubusercontent.com/58458582/84673794-22e1c300-af65-11ea-8740-cab856285273.PNG)
	* ![dbca 8 체크 해제](https://user-images.githubusercontent.com/58458582/84673795-237a5980-af65-11ea-9056-0f5ad1ee0aca.PNG)
		* 체크 해제
	* ![dbca 9 üũ](https://user-images.githubusercontent.com/58458582/84673796-237a5980-af65-11ea-83af-109e343f3888.PNG)
		* 샘플 스키마 체크
	* ![dbca 10 메모리 주기](https://user-images.githubusercontent.com/58458582/84673800-2412f000-af65-11ea-82ef-3a3c0b0ad6a4.PNG)
		* 메모리 주기
	* ![dbca 11 유니코드 설정](https://user-images.githubusercontent.com/58458582/84673802-24ab8680-af65-11ea-8e78-5047e786572f.PNG)
		* 유니코드 체크
	* ![dbca 12 next](https://user-images.githubusercontent.com/58458582/84673803-24ab8680-af65-11ea-8e06-d15f46703cb0.PNG)
	* ![dbca 13 finish](https://user-images.githubusercontent.com/58458582/84673805-25441d00-af65-11ea-8272-1e8a4f5b25aa.PNG)

