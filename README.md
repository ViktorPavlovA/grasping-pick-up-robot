# Курсовой проект 

**Тема: Применение Q-learning для обучения робота**

Выполнили: Павлов В. А, Горин Н. В, Сизов Е.В, Матвеев К. А

# Необходимые зависимости 

**Внимание для корректной работы используйте OS Ubuntu 20.04**


## Первое, что нужно сделать это установить anaconda

[Здесь](https://www.anaconda.com/products/distribution)

## После установки

1. Перейти в приложение  Anaconda Prompt (Anaconda3)

`dir` - посмотреть содержимое директории

`cd _папка_` - переход в **_папку_**

`mkdir grasping_conda` - создать папку **grasping_conda**

Простой пример:

`(base) C:\Users\Viktor>cd Desktop`

Я установил среду в папке на рабочем столе:

`(base) C:\Users\Viktor\Desktop>mkdir grasping_conda`

`cd grasping_conda`

2. В папке установим среду

`conda create -n grasp_env python=3.6`

**Эту команду нужно вбивать при запуске командной строки**

`conda activate grasp_env`

3. Перед установкой следующего пакета необходимо перейти в папку где у вас храниться anaconda 

`anaconda anaconda3>Library>bin`

**Найдите эти два файла:**

`libcrypto-1_1-x64.dll`

`libssl-1_1-x64.dll`

**и скопируйте в anaconda3>DLLs**

4. Установим дополнительные пакеты

`conda install git`

`git clone https://github.com/BarisYazici/deep-rl-grasping.git`

`conda install -c conda-forge cudatoolkit=10.0 cudnn=7.6.5`

`SET LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/`

5. Изменим setup.py

Для этого выполним предполагается, что у вас установлен vscode

[VSCODE](https://code.visualstudio.com/download)

В принципе подойдет любой текстовый редактор

`code .`

`'tensorflow==1.14.0'`

На

`'tensorflow_gpu==1.14.0'`

## Финальная установка

`pip install -e .`

## Возможные проблемы с пакетом ##

In this package trouble 'pybullet==3.2.5'

error: Microsoft Visual C++ 14.0 or greater is required. Get it with "Microsoft C++ Build Tools": 

**Установить и докачать пакеты**

https://visualstudio.microsoft.com/visual-cpp-build-tools/

**Возможно, придется в ручную прописывать все пакеты из setup.py**
        'stable-baselines==2.10.1',
        
        **Если вы тренируете на процессоре**
        
        'tensorflow==1.14.0',
        
        **Если вы тренируете на видеокарте**
        
        'tensorflow_gpu==1.14.0',
       
        'gym==0.19.0',
        
        'keras==2.2.4',
        
        'matplotlib==3.3.4',
        
        'numpy==1.18',
        
        'opencv-contrib-python==4.5.5.64',
        
        'pandas==1.1.5',
        
        'pybullet==3.2.5',
        
        'pytest==7.0.1',
        
        'pydot==1.4.2',
        
        'PyYAML==5.4.1',
        
        'seaborn==0.11.2',
        
        'scikit-learn==0.24.2',
        
        'tqdm==4.64.0',
        
        'paramiko==2.10.3',
