# Desarrollo de Interfaces - Diseño nativo I
  El objetivo de esta praćtica es conocer algunas de las tecnologías de diseño nativo. En esta sesión nos centraremos en tecnologías de escritorio.
  
* Diseño multiplataforma vs diseño nativo
   Como hemos visto en la práctica anterior, existen multitud de plataformas sobre las que desarrollar aplicaciones. Cada una de ellas tiene sus propios lenguajes y sus particularidades.

   Las ventajas y desventajas de un diseño multiplataforma son claras: obtenemos *sencillez* y un *único código* a cambio de *rendimiento*, *personalización* o acceso a determinadas *características específicas* de los sistemas operativos subyacentes.

   En este vídeo de Microsoft se analizan los pros y los contras de algunas de estas tecnologías: https://youtu.be/4m7msadL5iA
   
* Paradigmas de diseño de Interfaces de Usuario (UI)
   Hay dos grandes enfoques en las metodologías de diseño de interfaces:
   
   - Diseño *imperativo* - El interfaz de usuario (estructura) se crea en algún lenguaje de descripción, normalmente basado en XML. El código de la aplicación posteriormente hace referencia a dicha estructura y procede a *cambiar* algunos elementos de ella. Por ejemplo, el código hace referencia a una etiqueta y cambia su texto.
   - Diseño *declarativo* - El interfaz de usuario (estructura) es inmutable y todos los elementos o pantallas están predefinidos. No obstante, existen elementos que están conectados con los datos de la aplicación y *reaccionan* a dichos cambios, provocando los cambios visuales correspondientes.
     
   Los frameworks más modernos ([Flutter](https://flutter.dev/), [SwiftUI](https://developer.apple.com/xcode/swiftui/), [ReactNative](https://reactnative.dev/)) están apostando por el modelo declarativo. Algunas referencias:
   - https://medium.com/@gusterwoei/declarative-ui-rolling-into-mobile-and-beyond-966f49d055f4
   - https://flutter.dev/docs/get-started/flutter-for/declarative
   
# Tareas a realizar
* Desarrollo de Interfaces nativos en Windows
    Tal como comentamos en la práctica anterior, Windows ofrece varias tecnologías: 
     - [WinUI 3](https://learn.microsoft.com/es-es/windows/apps/winui/winui3/)
     - [Windows Presentation Foundation (WPF)](https://docs.microsoft.com/es-es/dotnet/desktop/wpf/)
      
    Se pide realizar el siguiente tutorial: https://docs.microsoft.com/en-us/learn/paths/develop-windows10-apps/. Tened en cuenta que configura Visual Studio para WinUI, pero que deberéis añadir también la configuración para WPF.

    Las *tareas* a realizar serán:
    - *Instalar* las herramientas de desarrollo (Visual Studio y SDKs de .NET framework)
    - Crear las *aplicaciones* de ejemplo que se proponen para [*WPF*](https://learn.microsoft.com/es-es/dotnet/desktop/wpf/get-started/create-app-visual-studio?view=netdesktop-8.0) y en [*WinUI*](https://learn.microsoft.com/en-us/windows/apps/how-tos/hello-world-winui3).
    - Adjunta una *captura de pantalla* de la ejecución de cada uno de los *dos proyectos* en la carpeta ```capturas``` del repositorio.
     
    Como resultado de la práctica se deben incluir los *dos proyectos* creados en Visual Studio. Ambas carpetas con los proyectos se añadirán a la *raíz* del repositorio.

    El repositorio lleva incluido un archivo ```.gitignore``` para Visual Studio: de esta manera solo se subirá el código al repositorio (no se subirán los ejecutables, archivos temporales o resultados de compilación).

    Por último, observa los archivos ~.xaml~ creados en cada uno de los proyectos. Son archivos de *descripción de interfaz de usuario* que crea el editor visual de Visual Studio. Investiga qué código corresponde a cada control de la aplicación. En el diseño de interfaces se puede trabajar con ese tipo de archivos o con editores visuales.
    
* Desarrollo de Interfaces con Python y GTK
    La segunda parte de la práctica trata sobre el desarrollo de interfaces con otra tecnología. Para ello utilizaremos [Python](https://www.python.org/) como lenguaje de programación y [GTK](https://www.gtk.org) como librería gráfica. Ambos son *multiplataforma*, por lo que la aplicación que se desarrolle se podrá ejecutar en Windows, GNU/Linux o MacOS X.

    La documentación sobre cómo trabajar con Python y GTK está disponible en https://www.gtk.org/docs/language-bindings/python/. En concreto, utilizaremos parte de este [tutorial de Python y GTK+ 3](https://python-gtk-3-tutorial.readthedocs.io/en/latest/).

    Las *tareas* a realizar serán:
    - [Instalar la librería GTK y Python](https://www.gtk.org/docs/installations/). A continuación se detallan las instrucciones para [Windows](https://www.gtk.org/docs/installations/windows/), por ser más complejas (tanto en GNU/Linux como en MacOS es más sencillo):
      - Descargar el paquete *msys2*: https://www.msys2.org/
      - Abrir la aplicación ```msys2 shell``` y ejecutar los siguientes comandos:
        - Instalar *GTK3*: ```pacman -S mingw-w64-x86_64-gtk3```
        - Instalar *Glade* (editor de interfaces): ```pacman -S mingw-w64-x86_64-glade```
        - Instalar la librería necesaria para que *Python* interactúe con *GTK*: ```pacman -S mingw-w64-x86_64-python3-gobject```
    - Instalar un editor *distinto del bloc de Notas de Windows*. Sugerencias: [Visual Studio Code](https://code.visualstudio.com/), [Notepad++](http://notepad-plus-plus.org/), [Sublime Text](https://www.sublimetext.com/),... Un editor específico para Python que es muy completo es [PyCharm](https://www.jetbrains.com/pycharm/).
    - Se utilizará el editor de texto para crear el programa en Python y *Glade* para crear el interfaz.
      - Para ejecutar *glade* en Windows es necesario abrir el programa ```mingw shell``` (instalado por msys2). En dicha ventana se ejecutará el comando ```glade``` para abrir dicho programa.
    - Crear una carpeta llamada ```python-gtk``` en la raíz del repositorio.
    - Leer el artículo [Getting Started](https://python-gtk-3-tutorial.readthedocs.io/en/latest/introduction.html) y crear el código propuesto en [Extended Example](https://python-gtk-3-tutorial.readthedocs.io/en/latest/introduction.html#extended-example) en un archivo llamado ```python1.py``` dentro de la carpeta ```python-gtk```. En lugar de mostrar el texto ```Hello World``` deberás mostrar tu *nombre y apellidos*.
    - Leer el artículo [Glade and Gtk.Builder](https://python-gtk-3-tutorial.readthedocs.io/en/latest/builder.html) y crear el código propuesto (los archivos se llamarán ```python2.py``` y ```python2-ui.glade``` respectivamente) dentro de la carpeta ~python-gtk~. En lugar de mostrar el texto ```Hello World``` deberás mostrar tu *nombre y apellidos*.
    - Adjunta una *captura de pantalla* de la ejecución de cada uno de los *dos proyectos* en la carpeta ~capturas~ del repositorio. Para lanzar los programas hay que ejecutar el comando ```python NOMBRE_ARCHIVO.py``` desde la consola de ```mingw```.

    Cuando termines, abre el archivo ```python2-ui.glade``` con el editor de textos y observa el código. Como puedes comprobar, el interfaz también está definido en XML (igual que en los proyectos de Visual Studio). De nuevo, investiga qué código corresponde a cada control de la aplicación.

    Por último, investiga algo más el programa ```Glade``` para crear alguna interfaz algo más compleja.
    
* Formato de la entrega
 - Cada alumno dispondrá de un repositorio en GitHub para su trabajo personal. Dicho repositorio se creará automáticamente al hacer clic en el enlace y aceptar la tarea (/assignment/).
 - Todos los archivos de la práctica se guardarán en el repositorio y se subirán a GitHub.
 - Se deberá entregar el código de los *4 proyectos* que se piden, así como *4 capturas de pantalla* que muestren la ejecución de dichos proyectos.
 - Para cualquier tipo de *duda o consulta* se pueden abrir ```Issues``` haciendo referencia al profesor mediante el texto ```@jsanz94``` dentro del texto del ```Issues```.
 - Una vez *finalizada* la tarea se debe crear un ```Issues``` en el repositorio haciendo referencia al profesor incluyendo el texto ```@jsanz94``` dentro del ```Issues```.
