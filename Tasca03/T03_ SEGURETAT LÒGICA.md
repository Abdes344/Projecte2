## T03:SEGURETAT LÒGICA 🔒🧠💻

![imatge](/Tasca03/IMG/1.png)

Abans de iniciar la máquina anem a la configuració per afegir un disc dur de seguretat  

---

![Imatge](/Tasca03/IMG/2.png)

Al entrar a la máquina virtual mantindrem el shift per entrar en aquest menú i seleccionarem la segona opció la de “Advanced options for zorin”.   

---

![](/Tasca03/IMG/3.png)

Després de entrar en la opció anterior ara tornarem a triar la segona opció “Zorin, with Linux 6.8.0-85-generic (recovery mode)”.   

---

![](/Tasca03/IMG/4.png)  

Entrarem en aquest menú de aqui i el que farem sera anar a la penúltima opción que es la de root i li donarem a enter per accedir  

---

![](/Tasca03/IMG/5.png) 

Després de entrar en el menu del root fiquem el següent codi per poder cambiar la contraseña “passwd miquel” després de ficar això ja podrem canviar la contrasenya

---

![](/Tasca03/IMG/20.png) 
.
![](/Tasca03/IMG/16.png)  

Després de canviar la contrasenya ens tornarà a sortir el mateix menú que abans y el que tindrem que fer sera donar li a la primera opció “Continuar con el arranque normal” y després de donar li a aquesta opció li donem a aceptar i ja haurem canviat la contrasenya

---

![](/Tasca03/IMG/22.png)  

Un cop dins de la maquina entrarem en el usuari que acabem de canviar la contrasenya i només ficant la contrasenya que hem ficat fa un moment ja estarem dins del usuari

---

![](/Tasca03/IMG/7.png)  

Al entrar a la màquina virtual entrarem a la terminal per ficar la següent comanda “sudo grub-mkpasswd-pbkdf2” i al ficar la comanda ens donara el hash de la nostra contrasenya  

---

![](/Tasca03/IMG/8.png)  

Per entrar en aquest apartat el que tindrem que fer sera fer el “sudo nano /etc/grub.d/40\_custom”

---

![](/Tasca03/IMG/9.png)  

Després de ficar la comanda anterior el que ficarem ara será el hash que van aconseguir de la comanda “sudo grub \-mkpasswd-pbkdf2” 

---

![](/Tasca03/IMG/10.png)  
![](/Tasca03/IMG/12.png)  

Ara actualitzarem amb la comanda “sudo update-grub” el que es fa amb aquesta comanda es actualizar el grub. I amb el següent comanda “sudo grub-mkconfig \-o /boot/grub/grub.cfg” el que farem amb aquesta comanda sera crear un nou arxiu de configuració 

---

![](/Tasca03/IMG/13.png)  
Després de reiniciar la maquina ens sortirà aquest apartat on tindrem que ficar el nom d'usuari i la contrasenya per poder entrar 

---

![](/Tasca03/IMG/14.png)    
✅ I Aquí ja estaria tot fet i només ficant la contrasenya ja estaria 🚀
