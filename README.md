# 5-bit 이진수 생성기
**문제**  
사용자에게 `n`을 입력받아 0 ~ 2^n-1 모든 이진수를 출력한다.

**해결 전략**  
- `range(2**n)` + `zfill(n)`  
- 잘못된 입력(음수·실수) Exception 처리

**빠른 실행**
```bash
python main.py 5
