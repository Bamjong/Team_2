# 22년 9월 20일 오전

## 오전 변경점

[com.victoree2.system]  
[SystemEx.java  // 51]

```java
case 4://언어선택
				change=!change;
				room.language = (change) ?  "kor" : "en";
				break;
```


    언어선택 토글로 바꿈


[com.victoree2.system]  
[SystemEx.java  // 27]

```java
user.load(); //로그인 체크를 위해 로그인 정보가 저장된 파일을 불러올것이다
			//관리자가 회원의 정보를 모두 보기위해 map값을 전부 가져옴
			Set<String> userMap = user.getAccount().keySet();
```

    hashmap 으로 전달하는 방식으로 바꿈	Hash


[com.victoree2.system]  
[AccountSystem.java  // 94]

```java
public AccountData login() {
		System.out.println(message(room.language, "0012"));
		System.out.println(message(room.language, "0008")+" " + message(room.language, "0009") + " : ");
		String id = scan.nextLine();
		System.out.println(message(room.language, "0010") + " " + message(room.language, "0009") + " : ");
		String password = scan.nextLine();
		AccountData returnValue=null;
```

    int 에서 AccountData로 바꾸어 계정정보를 return 하도록 바꿈
    유저DB 자체를 리턴받아서 값을 활용한 후 유저 정보를 활용할 수 있게


## 한 일

- print 정리(유저, 관리자)
- 기준 정리 (class명, 변수명 기준 잡기)