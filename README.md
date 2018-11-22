# EncodingTest
This is for encoding test.


# [UTF-8] 
## 한글 2 Byte, 영어 1 Byte, EOF 3 Byte ㄷㄷ
1한글 : 6 Byte
2한글 : 9 Byte
2한글 + 1영어 : 10 Byte
1영어 : 4 Byte
2영어 : 5 Byte

# [ANSI] 
## 한글 2 Byte, 영어 1 Byte, EOF 안 붙음
1한글 : 2 Byte
2한글 : 4 Byte
2한글 + 1영어 : 5 Byte
1영어 : 1 Byte
2영어 : 2 Byte

# [EUC-KR]
## 한글 2 Byte, 영어 1 Byte , EOF 안 붙음
1한글 : 2 Byte
2한글 : 4 Byte
2한글 + 1영어 : 5 Byte
1영어 : 1 Byte
2영어 : 2 Byte

## 특이사항
'꿿' 같은 글자는 표현 못 함

# [UTF-16 Little endian]
## 한글 2 Byte, 영어 2 Byte, EOF 2 Byte, But, BMP에 없는 문자의 경우 4(2*2) Byte
1한글 : 4 Byte
2한글 : 6 Byte
2한글 + 1영어 : 8 Byte
1영어 : 4 Byte
2영어 : 6 Byte
