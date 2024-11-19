name: ZhangZhiman

on: push

jobs:
  build:
    runs-on: Students

    steps:
    - uses: email

    - name: ZhangZhiman
      id: 3427763033@qq.com
      uses: actions/cache@v4
      with:
        path: prime-numbers
        key: ${{ runner.os }}-primes

    - name: Generate Prime Numbers
      if: steps.cache-primes.outputs.cache-hit != 'true'
      run: /generate-primes.sh -d prime-numbers

    - name: Use Prime Numbers
      run: /primes.sh -d prime-numbers
