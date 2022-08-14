# BROMA-PYTHON-CICLO-DE-MENSAJES
BROMA PARA ENVIAR MENSAJES DE FORMA CÍCLICA

1) primero importamos keyboard, en el terminal digita lo siguiente
```
pip install keyboard
```


```python
import keyboard
import time
import threading
```

2) luego de ello escribimos lo siguiente.

```python
import keyboard

#escribe la palabra en teclado
keyboard.write("Hermana.")
#presiona el comando enter
keyboard.press_and_release("enter")
```

en este caso le enviare mensajes a mi hermana, repitiendo hermana, si damos play en este momento veremos que la funcion se ejecuta una sola vez.
pues nosotros queremos que se repita cientos de veces. jejejjeejj. ![image](https://user-images.githubusercontent.com/66834393/184557721-1c6ec653-e47b-490a-aa0e-6a648348de73.png)

3) Entonces para ello haremos uso de un hilo que constantemente ejecute una acción, en resumen copia el siguiente codigo.

```python
import keyboard
import time
import threading

def enviar():
    #siempre se ejecute
    while(True):
        #esperamos 0.1 segundos hasta que vuelva a enviar
        time.sleep(0.1)
        # escribe la palabra en teclado
        keyboard.write("Hermana.")
        # presiona el comando enter
        keyboard.press_and_release("enter")
#Esperamos 3 segundos hasta que inicie
time.sleep(3)
#Inicializamos un objeto hilo cuyo objetivo será la función enviar()
hilo = threading.Thread(target=enviar())
#Iniciamos el hilo y disfrutamos el holocausto
hilo.start()
```

Y si, con esto lograras amargar a más de una persona. Éxitos te invito a que te suscribas y así poder subir mucho más contenido.
https://www.youtube.com/ingenieriajhr
![vidagithub](https://user-images.githubusercontent.com/66834393/184557996-c076c488-8659-45e8-a672-5f7d1848b886.png)




