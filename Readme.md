# Arquitectura de Xamarin Forms

El componente principal es una clase llamada **App**, dentro de esta clase se establecen:

+ La raíz visual de la aplicación **(MainPage)**.
+ Establecer recursos globales de la aplicación **(Resources)**.
+ Eventos del ciclo de vida de la aplicación.
+ Propiedades de la aplicación.



```c#
public partial class App : Application
    {
        public App()
        {
            InitializeComponent();

            MainPage = new MainPage();
        }

        protected override void OnStart()
        {
            // Handle when your app starts
        }

        protected override void OnSleep()
        {
            // Handle when your app sleeps
        }

        protected override void OnResume()
        {
            // Handle when your app resumes
        }
    }
```

Cada plataforma de aplicación (Android y iOS) tiene su propio modelo de aplicación de manera que se debe respetar la API o SDK  de la plataforma en  la que desarrollemos.

# Jerarquía de Clases

La clase base y de la que heredan todas las demás clases en *Xamarin* es la clase:

 ***BindeableObject*** donde se encuentran el *Sistema de propiedades enlazables y Notificaciones*.

***Element***, es la clase base de los elementos jerárquicos.

***VisualElement***, Clase base de los elementos interactivos y visuales.

***Cell***, Clase base para todas las celdas de las listas.

***View***, Clase base para todos los controladores.

***Page***, Clase base para todas las  páginas o pantallas.

***Layout<T>***, Clase base para todos los elementos de distribución en pantalla y paneles contenedores.