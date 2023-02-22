
# Para utilizar o simulador completo é preciso ter:

Ubuntu 20.04 LTS

<code>wget -c https://raw.githubusercontent.com/qboticslabs/ros_install_noetic/master/ros_install_noetic.sh && chmod +x ./ros_install_noetic.sh && ./ros_install_noetic.sh</code>

Digite a senha do usuário para os comandos sudo

Escolha a opção '1' para instalar o ROS completo

<code>sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential -y</code>

<code>git clone --recurse-submodules https://github.com/lmartim4/Mandi2-Simulador.git</code>

<code>cd Mandi2-Simulador/</code>

<code>git submodules init</code>

<code>git submodules update</code>

<code>catkin_init</code>

<code>catkin_make //5 vezes até dar certo</code>
