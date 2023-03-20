# Web UI + Stable Diffusion Guide (Ko Ver)

## 1. Web UI Git 가져오기
> $ git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git

## 2. Web UI 사용하기
### 경로 설정 
- 내 PC → C: → MY FOLDER(자유롭게 폴더 하나 생성) → Stable-diffusion-webui

- > $ webui-user.bat 실행

- To create a public link, set 'share=true' in 'launch()' 문구 발생 시 다운로드 완료 된 것이다.

### 접속 하기
- http://127.0.0.1:7860

(이후 접속 하려면, webui-user.bat 실행 후 "To creat ~ " 문구 발생 시 위 링크 접속하면 된다.) 

## 3. Stable Diffusion 사용하기 (그림체 셋팅)
- 나는 Web UI를 활용하여 만화 스타일로 그림 그리는 방법을 택했다.
- [그림체 사이트](https://civitai.com/)
- 이미지 왼쪽 상단에 Checkpoint 라고 되어있는 그림 스타일 중 원하는 항목을 골라 다운로드 받아준다. (로그인 해야 항목이 확 늘어나기 때문에 꼭 로그인)
    - checkpoint 경우 "C:\stable-diffusion-webui\models\Stable-diffusion" 경로에 파일을 넣어준다.   
- 이후, 보정을 해주는 VAE를 받아주면 끝이 난다.
    - "C:\stable-diffusion-webui\models\VAE" 경로에 파일을 넣어준다.

## 4. 위의 설정이 다 끝났다면...
- 링크에 접속을 하여 "Stable Diffusion Checkpoint" 에서 다운 받은 Checkpoint를 선택하고 몇 분정도 기다리면 적용이 된다.
- 그 다음, Setting 메뉴를 누른 뒤 "Stable Diffusion" 탭을 누르고 이후 SD VAE 밑에서 다운로드 받은 VAE 파일을 넣어주고 Apply Settings를 클릭한다.
- 이제, txt2img 로 들어와 그리고 싶은 내용을 입력하면 된다. 

## 5. LORA 사용
- LORA를 사용하기 위해 다운로드 받은 파일을 다음과 같은 경로에 넣어준다.
    - C:\stable-diffusion-webui\models\Lora
- 다시 Web UI를 실행한다.
- txt2img 탭에서 LORA 탭으로 들어오면 아까 전에 다운로드 받은 파일을 누르게 되면 "lora:############v15:1" 식으로 프롬프트 맨 끝에 배치된다.
    - 1은 인물을 모두 LORA를 참조해 가져오겠다는 얘기이다.
    - 추가적으로, 0.4라면 0.4 정도만 참조하겠다는 얘기이다.

- 이후, LORA를 넣어주어 Generate 하면 된다.