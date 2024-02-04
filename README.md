# Worker Guide
## 1. Register new horde account
- Click the link below.

  ↓↓↓

  [Register new horde account](https://stablehorde.net/register)

- You will be redirected to Horde registration page. Choose >> **Sign in with google**  

  <kbd>![regaccc](https://github.com/Neron-25/AIhorde-guide/assets/127858929/2dcc616b-3a82-4356-9397-149e978ead53)</kbd>


- Choose your google account >> agree and continue  

- Set **Display name \*** >> Input any desired name of your future account

- After that You will be provided with **API key** (highlighted by orange). **Save it anywhere, nobody will save it except You**

  <kbd>![apikeyt](https://github.com/Neron-25/AIhorde-guide/assets/127858929/2351b3c9-629e-4f25-a41a-805163c9d760)</kbd>

## 2. Set and run Google colab worker

- Visit the link below.

  ↓↓↓

  [Google colab Worker](https://stablehorde.net/register)

- Firstly you should input settings of your worker:
  
  - **worker_name:** Create unique name for your worker, all next times you will run the worker you should **reuse** this name (worker stats are attached to its name)
  - **api_key:** Input your API key
  - **max_power** This changes max resolution of images worker can process, for example: 32 - 1024 x 1024, 50 - 1280 x 1280. (Personally I run at 40 for usual works and 32 for post processing works)
  - **recommended_model1:** Choose one from most popular models you want to host. **It shouldnt be SDXL model** (google colab doesnt support it because of lack of power, but if you run paid colab version you might try)
  - **recommended_model2:** Dont choose, leave as None, except you are using paid colab version.

    <kbd>![colab1](https://github.com/Neron-25/AIhorde-guide/assets/127858929/f725a1ec-8934-44a9-83ce-86cfb982e697)</kbd>

- If you want to run specific model - set **recommended_model1:** and **recommended_model2:** to None, choose desired model in **model1**. 

  <kbd>![anothermodel](https://github.com/Neron-25/AIhorde-guide/assets/127858929/d7378a4b-cb3a-401d-8d25-61d05f59313e)</kbd>

- Post processing and experimental:
  - You might want to enable **allow_post_processing:** (it enables things such as upacalers and face improvers for you worker, in this case I recommend set **max_power** around 32)
  - **allow_controlnet:** - enables controlnet. (advanced img2img)
 
    <kbd>![postprocesss](https://github.com/Neron-25/AIhorde-guide/assets/127858929/291232ad-d488-487c-85fb-e66c24cf9f4d)</kbd>

  - Enable **experimental** and **batching_switch** (not necessary but recommended; usually I set **max_batch** to 3, but you might play around it and see how much your worker can handle)
    
    <kbd>![experim](https://github.com/Neron-25/AIhorde-guide/assets/127858929/d35ffcde-7286-4be5-a546-ac68c6eedea4)</kbd>

- Run all cells: Runtime -> run all (CTRL + F9).
  
  <kbd>![fdsfsa](https://github.com/Neron-25/AIhorde-guide/assets/127858929/7613674e-8607-491a-be8c-d09e98a0b49a)</kbd>

- Wait till all cells will be executed and last one **7.- Run the worker** starts. There logs will be appear and from time to time you need to clear them (hover your mouse over three dots and click); or there is option to disable them: just uncheck **Short_logs** in 0 cell.

  <kbd>![nwmnebf](https://github.com/Neron-25/AIhorde-guide/assets/127858929/bdab6f17-6e53-4998-b84c-1fd5ab4dbd34)</kbd>

Averagely colab runs for ~ 6 hours and after ~ 3 hrs there will be an alert where you should check "Im not a robot". You can try creating multiple google accounts to run several workers (one account can run only one worker at time), and you will need to create other unique names for new workers.
