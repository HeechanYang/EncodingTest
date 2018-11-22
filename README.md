# EncodingTest
This is for encoding test.


# UTF-8 
### 한글 2 Byte, 영어 1 Byte, EOF 3 Byte 
- 1한글 : 6 Byte  
- 2한글 : 9 Byte  
- 2한글 + 1영어 : 10 Byte  
- 1영어 : 4 Byte  
- 2영어 : 5 Byte  

# ANSI 
### 한글 2 Byte, 영어 1 Byte, EOF 안 붙음
- 1한글 : 2 Byte  
- 2한글 : 4 Byte  
- 2한글 + 1영어 : 5 Byte  
- 1영어 : 1 Byte  
- 2영어 : 2 Byte  

# EUC-KR
### 한글 2 Byte, 영어 1 Byte , EOF 안 붙음
- 1한글 : 2 Byte  
- 2한글 : 4 Byte  
- 2한글 + 1영어 : 5 Byte  
- 1영어 : 1 Byte  
- 2영어 : 2 Byte  

### 특이사항
- '꿿' 같은 글자는 표현 못 함

# UTF-16 Little endian 
### 한글 2 Byte, 영어 2 Byte, EOF 2 Byte, But, BMP에 없는 문자의 경우 4(2*2) Byte
- 1한글 : 4 Byte  
- 2한글 : 6 Byte  
- 2한글 + 1영어 : 8 Byte  
- 1영어 : 4 Byte  
- 2영어 : 6 Byte  

### 특이사항
- Windows Pro 10 기준, notepad를 통해 인코딩 설정을 할 때 '유니코드'라고 저장하면 'UTF-16 LE'로 저장됨.
    - '유니코드'는 '인코딩 표준'중 하나이기 때문에 '유니코드'로 저장할 수는 없고, '구현체'(UTF-8, UTF-16, etc.. )로 저장해야함
        - Java의 'Interface'와 그것을 'Implement한 Class'같은 느낌이군
    - 결론 : '유니코드'라고 표기한건 잘못이며 UTF-16 LE와 같은 형식으로 표기해야 함.

# 참고할 만한 문헌
https://stackoverflow.com/questions/13894898/unicode-file-in-notepad

https://enjoydoingitwrong.wordpress.com/2009/06/22/unicode-is-not-utf/