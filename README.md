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

`conda create -n любое_имя python=3.6`

**Эту команду нужно вбивать при запуске командной строки**

`conda activate любое_имя `


4. Установим дополнительные пакеты

`conda install git`

`git clone https://github.com/ViktorPavlovA/grasping-pick-up-robot.git`

`conda install -c conda-forge cudatoolkit=10.0 cudnn=7.6.5`

`export  LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/`

5. Изменим setup.py

Для этого выполним предполагается, что у вас установлен vscode

[VSCODE](https://code.visualstudio.com/download)

В принципе подойдет любой текстовый редактор

`code .`

`'tensorflow==1.14.0'`

у нас с ребятами gpu, поэтому мы выбрали 2 вариант

`'tensorflow_gpu==1.14.0'`

## Финальная установка

`pip install -e .`

## Как обучать ?

**Выбор алгоритма**

`--algo SAC or DQN`   

**Куда сохранется**

`--model_dir trained_models/SAC_best_shot` 

**Запуск**

`python manipulation_main/training/train_stable_baselines.py train --config config/gripper_grasp.yaml --algo SAC --model_dir trained_models/SAC_best_shot --timestep 100000 -v `  

## Обработка результатов эксперемента

**запуск из корня проекта**

`python scripts/plot.py --log-dirs trained_models/DQN_best_shot/`

