# Processo para utilização do Buildozer
## Esse procedimento foi o processo de tentativa e erro o qual passei para conseguir fazer a compilação de um aplicativo mobile android.

> verificar se o pip esta instalado:

     pip -V

 1.  se não tiver nenhuma versão instalada: https://bootstrap.pypa.io/get-pip.py 
 2. `sudo python3 get-pip.py`
 3. Se der erro ao instalar colocar o código abaixo e repetir o processo 2
	 3. 1  `sudo apt-get install python3-distutils`
##
### INSTALAR O KIVY
**instalação manual de suas dependências:**

    sudo apt-get install -y \
    		 python3-pip \
    		 build-essential \
    		 git \
    		 python3 \
    		 python3-dev \
    		 ffmpeg \
    		 libsdl2-dev \
    		 libsdl2-image-dev \
    		 libsdl2-mixer-dev \
    		 libsdl2-ttf-dev \
    		 libportmidi-dev \
    		 libswscale-dev \
    		 libavformat-dev \
    		 libavcodec-dev \
    		 zlib1g-dev
**Fazer instalação do cython**

    sudo pip3 install cython

**fazer instalação do KIVY**

    sudo pip3 install kivy
##
### INSTALAR BUILDOZER
    

> ***Instalar dependencias do buildozer:***
https://buildozer.readthedocs.io/en/latest/installation.html#targeting-android

**verificar o que manda ser feito:** 
Na versão atual do linux esta sendo passado o seguinte código a ser instalado:

    sudo apt update
    sudo apt install -y git zip unzip openjdk-8-jdk python3-pip autoconf libtool pkg-config zlib1g-dev libncurses5-dev libncursesw5-dev libtinfo5 cmake libffi-dev libssl-dev
    pip3 install --user --upgrade Cython==0.29.19 virtualenv

**Instalar as lib:**
  
    sudo apt-get install libltdl-dev libffi-dev libssl-dev autoconf autotools-dev

> ***Instalar o BUILDOZER:***
> https://kivy.org/doc/stable/guide/packaging-android.html#packaging-your-application-into-apk

    git clone https://github.com/kivy/buildozer.git
    cd buildozer
    sudo python3 setup.py install
##
### CRIAR APK
    

> Na pasta raiz do projeto.

    buildozer init
    buildozer android debug deploy run
