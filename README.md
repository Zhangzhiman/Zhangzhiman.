name: ZhangZhiman

on: push

jobs👩‍🎓
  build
    runs-on: 

    steps:
    - uses: email

    - name: ZhangZhiman
      id: 3427763033@qq.com
      uses: QQ
      with:
        path: 3427763033
        key: Learning and communication

    - name: Tentative
      if: steps.cache-primes.outputs.cache-hit != 'true'
      run: /generate-primes.sh -d prime-numbers

    - name: Use Prime Numbers
      run: /primes.sh -d prime-numbers
