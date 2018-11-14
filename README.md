# MLVRS-Numerico-Simulacion
En este repositorio podremos encontrar el código del programa Stochastic Lotka-Volterra Model Simulator, con el cual se pueden crear simulaciones basadas en agentes (utilizando Monte Carlo) de la dinámica de un sistema depredador-presa, en donde los depredadores se mueven aleatoriamente siguiendo una distribución de pasos del tipo ley de potencias con exponente $\beta$. Las presas se mantienen localizadas dentro de un parche (circulo) de radio $R$; pueden reproducirse, dentro del parche, con una tasa de crecimiento $\sigma$, mientras que los depredadores pueden alimentarse de ellos con una probabilidad $\lambda'=1$. Cuando un depredador encuentra a una presa, este puede reproducirse con una probabilidad $\lambda$. Los depredadores, además de moverse libremente en un espacio infinito, pueden realizar una relocalización estocástica al centro del parche, con una distribución exponencial de tiempos de relocalización a tasa $r$. Esta simulación está basada en la dinámica presentada en el trabajo "Sistemas de Lotka-Volterra con relocalización estocástica", el cual es un trabajo de maestría escrito por José Gabriel Mercado Vásquez, y dirijido por el doctor Denis Pierre Boyer. En el siguiente enlace encontrará el trabajo publicado en la revista científica Journal of Physics A:Mathematical and theoretical https://doi.org/10.1088/1751-8121/aadbc0.

A continuación describimos el contenido del repositorio SLVMSimulator:

* En la carpeta lotkaresetting encontraremos el código completo del programa SLVMSimulator, el cual nos desplega en pantalla un menú interactivo, mediante el cual podremos cambiar los parámetros del sistema, como lo son aquellos de movilidad: $\beta$, $r$; los parámetros demográficos $\lambda$, $\sigma$, población inicial de depredadores y de presas, radio del parche $R$; tiempo de Monte Carlo y un parámetro llamado $zoom$ que es únicamente para hacer los gráficos más grandes o más pequeños. En este menú también podremos alegir un archivo en el cual se guardarán los datos relevantes en la realización de una simulación (población de presas y de depredadores, así como el tiempo de ejecución del programa). Encontraremos información del programa en la sección de ayuda, en el menú. Dado que este programa necesita varios métodos, el código se divide en varios archivos. En cada archivo encontrará su correspondiente descripción.

* En la carpeta graphics encontramos el logo del programa SLVMSimulator, el cual será necesario para poder compilarlo y hacer el que programa desplegue un ícono.

* En la carpeta principal se localiza el archivo SLVMSimulator.jar, que es el ejecutable compilado del programa descrito en el primer punto. Se podrá abrir al tener instalado Java en su computadora. https://www.java.com/en/download/

* En la carpeta src encontrará el programa SLVMSimulator en una versión no gráfica, mediante la cual se pueden realizar varias simulaciones, guardando los datos resultantes de la simulación (población de depredadores y de presas, tiempo de ejecución, parámetros de movilidad y demográficos).

* En la carpeta Wolfram se encuentran dos archivos de ejecución con extensión .wls. Con estos programas se resolvió numéricamente el modelo Lotka-Volterra con reinicio estocástico en 1D. El archivo resuelvea0.wls resuelve numéricamente la ecuación (12) del artículo citado anteriormente, para obtener la densidad de presas en el parche, y con ello obtener la población total de depredadores (ecuación 10). La población total es calculada en función de los parámetros demográficos y de movilidad. Estos datos se analizan con el programa maxerebta.wls para obtener aquellos valores de $\beta$ y $r$ que maximizan la población. 
