### `tr` 명령어의 약어

`tr` 명령어는 **Translate**의 약어로, 입력된 텍스트의 문자를 다른 문자로 변환하거나 삭제하는 데 사용되는 리눅스/유닉스 명령어입니다. 주로 텍스트 스트림에서 특정 문자를 다른 문자로 대체하거나, 반복되는 문자를 제거하는 등의 간단한 텍스트 변환 작업에 활용됩니다.

#### 주요 기능:
1. **문자 변환**: 지정된 문자 집합을 다른 문자 집합으로 변경합니다.
   ```bash
   echo "hello" | tr 'h' 'H'  # 출력: Hello
   ```
2. **문자 삭제**: 특정 문자를 삭제합니다.
   ```bash
   echo "hello" | tr -d 'l'  # 출력: heo
   ```
3. **문자 압축(스퀴즈)**: 반복되는 문자를 하나로 압축합니다.
   ```bash
   echo "helloooo" | tr -s 'o'  # 출력: helloo
   ```

#### 사용 예시:

- **소문자를 대문자로 변환하기**
  ```bash
  echo "hello world" | tr 'a-z' 'A-Z'  # 출력: HELLO WORLD
  ```

- **특정 문자를 제거하기**
  ```bash
  echo "hello 123 world" | tr -d '0-9 '  # 출력: helloworld
  ```

- **여러 공백을 하나의 공백으로 압축하기**
  ```bash
  echo "This    is  a    test." | tr -s ' '  # 출력: This is a test.
  ```

#### 추가 정보:
`tr` 명령어는 파일을 직접 읽지 않고, 표준 입력을 통해 데이터를 처리하기 때문에 파이프(`|`)와 함께 자주 사용됩니다. 이를 통해 복잡한 텍스트 변환 작업을 간단하게 수행할 수 있습니다.

#### 참고 자료
- [GeeksforGeeks - tr command in Unix/Linux with examples](https://www.geeksforgeeks.org/tr-command-in-unix-linux-with-examples/)
- [IBM Documentation - tr Command](https://www.ibm.com/docs/en/ssw_aix_71/t_commands/tr.html)
- [Man7.org - tr(1) Manual Page](https://man7.org/linux/man-pages/man1/tr.1.html)

이해에 도움이 되었기를 바랍니다! 추가적인 질문이 있으시면 언제든지 문의해 주세요.