
# Para utilizar o simulador completo é preciso ter:

Ubuntu 20.04 LTS

<code>wget -c https://raw.githubusercontent.com/qboticslabs/ros_install_noetic/master/ros_install_noetic.sh && chmod +x ./ros_install_noetic.sh && ./ros_install_noetic.sh</code>

Digite a senha do usuário para os comandos sudo

Escolha a opção '1' para instalar o ROS completo

<code>sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential -y</code>

<code>git clone --recurse-submodules https://github.com/lmartim4/Mandi2-Simulador.git</code>

<code>cd Mandi2-Simulador/</code>

<code>catkin_make //5 vezes até dar certo</code>

<code>source devel/setup.bash</code> //Esse comando deve ser executado sempre se quiser usar essa instalação do Simulador. Pode ser adicionado ao .bashrc para praticidade extra
 
<code>roslaunch uuv_gazebo_worlds ocean_waves.launch</code> //Para testar se tudo está funcionando
<code>roslaunch uuv_descriptions upload_rexrov.launch mode:=default x:=0 y:=0 z:=-20 namespace:=rexrov</code>
<code>roslaunch uuv_control_cascaded_pid joy_velocity.launch uuv_name:=rexrov model_name:=rexrov joy_id:=0</code>
<code>roslaunch uuv_teleop uuv_keyboard_teleop.launch uuv_name:=rexrov2<code>
