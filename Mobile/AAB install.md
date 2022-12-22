# [AAB 파일 설치 순서]
1. 사전에 AAB파일, KeySotre 파일, KeyStore ks-pass(키 저장소 비밀번호), key-pass(서명자 비공개키 비밀번호), Keystore ks-alias(키 저장소 별칭) 정보를 전달 받는다.
2. https://github.com/google/bundletool/releases 주소에서 bundletool jar 파일을 다운로드 받는다.
3. 아래 명령어를 입력하여 AAB 파일을 복호화 한다.
   java -jar bundletool 경로 build-apks --bundle=AAB 파일 경로  --output=추출하여 저장할 파일 경로 --ks=KeySotre 경로 --ks-pass=Keystore 키 패스워드 --ks-key-alias=KeyStore 별칭 --key-pass=서명자 키 패스워드 --mode=universal
4. 복호화 진행이 완료되면 apks 파일이 --output 옵션 내 입력했던 경로에 저장이 됨
5. apks 파일의 확장자를 zip 확장자로 변경
6. zip 파일의 압축 해제하면 apk 파일이 추출 됨
7. 해당 apk 파일을 adb 이용하여 단말 내 설치