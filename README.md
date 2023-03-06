# Excel2chatGPT

##### 📑 EXCEL <--->  ChatGPT 🤖

excel2chatgpt is a command line tool that uses [ChatGPT](https://openai.com/blog/chatgpt/)'s artificial intelligence to populate Excel files with coherent and engaging responses based on cell contents. It's easy to use and can save time and effort in various tasks.

🛟 Find help in [Telegram](https://t.me/+TuRPrGt5zZoyZjlh)


📦 [Downloads](https://github.com/jfadev/excel2chatgpt/releases)

## Install

Requirements: [nodejs](https://nodejs.org/) >=18 (Latest [maintenance LTS](https://github.com/nodejs/Release#release-schedule) version),
 [npm](https://www.npmjs.com/), [chrome/chromium](https://www.chromium.org/chromium-projects/) and [OpenAI credentials](https://openai.com/blog/chatgpt/)

```bash
$ npm install
```

## Configuration

Edit `.env` file

License Key:
(Free mode is limited to 5 iterations. 
Unlock this limitation by purchasing 
a license at https://jordifernandes.com/excel2chatgpt)
```javascript
LICENSE="free"
```

OpenAi credentials:
```javascript
OPENAI_EMAIL="your@mail.com"
OPENAI_PASSWORD="yourpassword"
```

Google Authentication (`1` true, `0` false):
```javascript
OPENAI_IS_GOOGLE=1
```

Use proxy ("`IP`:`PORT`"):
```javascript
PROXY_SERVER="127.0.0.1:8008"
```

Input/Output of XLSX file:
```javascript
INPUT="./example.xlsx"
OUTPUT="./example.xlsx"
```

Global concatenation before and after prompt:
```javascript
PROMPT_PREFIX="Describe in 15 words:"
PROMPT_SUFFIX=""
```

First row of the XLSX where a read begins:
```javascript
FIRST_ROW=2
```

Prompt Cell position in XLSX file:
```javascript
PROMPT_CELL=1
```

Result Cell position in XLSX file:
```javascript
RESULT_CELL=2
```

Overwrite result column (`1` true, `0` false):
```javascript
OVERWRITE_RESULT_CELL=1
```

Milliseconds to wait between each iteration:
(use "AUTO" for random values between `MIN` and `MAX` ms.
chatGPT may limit for excessive requests with a 429 error):
```javascript
ITERATION_TIME_SLEEP=15000
```
If use `AUTO` set `MAX` and `MIN`
```javascript
ITERATION_TIME_SLEEP_MIN=150
ITERATION_TIME_SLEEP_MAX=80000
```


Milliseconds to wait if ChatGPT return error "too many requests":
(default 5 mins)
```javascript
TOO_MANY_REQUESTS_TIME_SLEEP=300000
```

##### Example
![Screeshot](doc/4.png?raw=true "Screeshot")


## Run

##### 1. Run
```bash
$ npm run start
```
##### 2. Solve the Captcha
![Screeshot](doc/1.png?raw=true "Screeshot")

##### 3. Working
![Screeshot](doc/2.png?raw=true "Screeshot")

##### 4. Result
![Screeshot](doc/3.png?raw=true "Screeshot")

## Authors

- [Jordi Fernandes (@jfadev)](https://github.com/jfadev)