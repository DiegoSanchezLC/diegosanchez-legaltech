---
{"dg-publish":true,"dg-path":" 3. Artículos de interés. /Las 15 mejores herramientas OSINT  Odin 2.md","permalink":"/3-articulos-de-interes/las-15-mejores-herramientas-osint-odin-2/","title":"Las 15 mejores herramientas OSINT | Odin","tags":["clippings"]}
---


EXTRAÍDO DE ODINT.NET.

Siempre es bueno insistir que, en OSINT, **las herramientas no son lo más importante**. Pero también es cierto que, sin aplicaciones y software especializado en fuentes abiertas, no llegaremos muy lejos en una investigación a fondo. Es por eso que, hoy, se muestran las **15 mejores herramientas OSINT** que, por experiencia, han resultado más útiles en investigaciones y actividades de ciberinteligencia.

Como siempre pasa con estas cosas, no será posible enumerarlas todas y habrá quien piense que hay grandes ausencias. Es normal. Este es el secreto de las herramientas OSINT cuando las utilizas en escenarios reales:

> Hay infinidad de aplicaciones y software de inteligencia de fuentes abiertas, pero apenas usaremos una fracción muy pequeña.

Esa fracción dependerá de los gustos del investigador y la naturaleza de los trabajos encomendados.

Por ejemplo, en muchos trabajos que se han hecho, ciertas herramientas comerciales SEO eran mucho más eficaces que herramientas tradicionales OSINT a la hora de encontrar la información e inteligencia deseadas.

Sin embargo, ciberinvestigadores de otros ámbitos, como la búsqueda de personas, apenas tocarán ese software.

## El mito de la herramienta perfecta y la que sirve para todo

El otro gran mito es que hay una herramienta perfecta. **No la hay**.

De la misma manera, **aplicaciones que tratan de abarcar mucho son más ineficaces que el uso de varias herramientas especializadas**. Es lo que hay en el mundo real.

Muchas veces, el uso de aplicaciones OSINT se basa en comenzar utilizando la preferida para obtener ese dato deseado y, si no, debemos conocer alternativas que, en ocasiones puntuales, puedan llegar donde las habituales se quedaron cortas.

Pero no nos entretengamos más y comencemos con las 15 mejores herramientas OSINT por experiencia.

## 1\. Google y sus operadores avanzados (Google Dorking)

![Google Dorking como herramienta OSINT](https://odint.net/images/google-dorking.webp)

Es inevitable empezar por aquí. Si bien los resultados de Google están empeorando en calidad a marchas forzadas, **sigue siendo la mejor herramienta OSINT que existe**.

Es por eso que todo ciberinvestigador debería usarla y, sobre todo, **estar familiarizado con sus operadores avanzados de búsqueda**, para delimitar bien dichas búsquedas y encontrar ese dato necesario en un mar de ruido cada vez más grande.

Al arte de buscar en Google con combinaciones de operadores avanzados, que nos devuelvan exactamente lo que queremos, se le llama *Google dorking*.

Así, hay combinaciones sencillas de *Google dorking*, como por ejemplo:

```fallback
site:elpais.es "término de búsqueda"
```

Para buscar solamente resultados en el diario El País que coincidan, exactamente, con el término de búsqueda y contenga todas las palabras de la frase en ese mismo orden.

Esas combinaciones de operadores avanzados pueden dar lugar a *dorks* más técnicos, como:

```fallback
"secreto" + "confidencial" filetype:pdf | filetype:doc | filetype:xlsx site:gov
```

Que buscará posibles documentos que se hayan dejado públicos por descuido, en formato Excel, Word o PDF, dentro de posibles dominios gubernamentales (anglosajones) y que contengan palabras que pueden llevar hasta archivos jugosos.

Es increíble lo que uno puede encontrar solo con Google en una labor OSINT y, antes de aprender más, **cualquier ciberinvestigador debería convertirse en un *ninja* de los operadores avanzados y el Google Dorking**.

Como referencia, hay miles de combinaciones interesantes de Google Dorking en la de Exploit Database.

## 2\. La búsqueda inversa de imágenes de los buscadores

No abandonamos Google y similares, porque la otra gran herramienta a la que recurres en casi todas las labores de ciberinteligencia es **la búsqueda inversa de imágenes**.

Es decir, que subes una imagen a un buscador como Google y este encontrará si hay coincidencias o algo parecido.

No podría ser más sencillo. Nos vamos a Google Imágenes, por ejemplo, pulsamos en el icono de fotografía y seleccionamos la opción “Subir una imagen”.

![Google Imágenes como herramienta OSINT](https://odint.net/images/google-images.webp)

En estos casos, es fácil descubrir:

- Fotos de perfil falsas que, en realidad, son de modelos o tomadas de otras personas en la red.
- Qué ubicación estamos viendo en la foto, gracias a encontrar imágenes similares que geolocalicen.
- Quién es esa persona que vemos en la foto en algunos casos.

Y mucho más.

La cuestión últimamente es esta, **por experiencia, la está resultado, en muchos casos, mejor que la de Google**.

Eso no significa dejar de lado Google, sino **utilizar también Bing y no subestimarlo**, nos podemos llevar más de una sorpresa.

Por supuesto, **también está** , imposible no nombrarla.

## 3\. GHunt, para encontrar datos sobre una cuenta de Google

![GHunt en acción, una de las mejores herramientas OSINT](https://odint.net/images/ghunt.webp)

Casi todo el mundo tiene correo en Gmail y cuenta en Google, por eso, es importante trabajar ese ángulo en cualquier investigación OSINT.

Y para extraer la mayor cantidad de datos de una cuenta Google, está , **una herramienta OSINT imprescindible** y excepcional.

Reseñas, el ID de Google del objetivo, canales de Youtube, localizaciones… Es fascinante lo que a veces puede encontrar esta herramienta.

Y sí, **es un pequeño dolor de cabeza instalar y configurar bien GHunt**, pero, en realidad, **no es tan difícil si sigues al pie de la letra las instrucciones**, especialmente, la parte de obtener dichosas *cookies* necesarias.

Personalmente, el método manual siempre ha funcionado sin problemas en cada equipo o máquina virtual configurada.

## 4\. Shodan, el buscador de dispositivos conectados a la red (y expuestos)

![La página principal de Shodan, una excelente aplicación OSINT](https://odint.net/images/shodan.webp)

Otro clásico en las investigaciones OSINT que, dependiendo del objetivo de las mismas, puede resultar muy útil.

Shodan.io es el **buscador de dispositivos conectados a la red** y puedes encontrar de todo, pero, especialmente, **se usa para encontrar aparatos comprometidos o expuestos**, como cámaras web o impresoras, aunque no solo eso, claro.

Puedes usar sus operadores para delimitar la búsqueda, pero necesitarás una cuenta de usuario para eso.

También tiene una versión de pago, con un coste único de 49 dólares, que te permite acceder a opciones más avanzadas y merece la pena si vas en serio.

En muchas ocasiones, salen cupones que rebajan ese precio. Imprescindible para ciberinvestigaciones más técnicas, tests de penetración, etc.

## 5\. Sherlock (o alternativas online) para encontrar nombres de usuarios en redes y webs

![Sherlock en acción](https://odint.net/images/sherlock.gif)

Una de los datos más habituales que se poseen en cualquier ciberinvestigación es un nombre de usuario. Encontrar en qué redes sociales está dicho usuario o variaciones de ese *nick* puede llevar a encontrar información muy interesante.

La herramienta clásica de OSINT, para investigar dichos nombres de usuario en multitud de redes sociales y webs, comprobando si existe, es .

No obstante, **hay bastantes alternativas online** (como por ejemplo, ) que nos pueden sacar del paso si no tenemos a mano la máquina virtual OSINT o a Sherlock.

*Spoiler:* **fallan muchísimo y no suelen dar muy buen resultado**. Muchas veces, te dicen que la cuenta no existe cuando sí lo hace, o al revés. Es **importante comprobar por uno mismo**.

## 6\. Have I been pwned? Para encontrar emails y teléfonos comprometidos

![La web de Have I been pwned?](https://odint.net/images/pwned.webp)

Este excelente buscador permite introducir un email o un teléfono y consultar si dicho correo o número **aparece en una de las muchas listas de datos *hackeados* y filtrados que existen.** Cada día va creciendo más y es un recurso imprescindible.

Su uso, eso sí, puede dar lugar a llegar hasta fuentes “abiertas” que quizá puedas o no usar en tu investigación. Todo depende de los parámetros de la misma, las restricciones legales, etc.

Por ejemplo, en un test de penetración para una compañía, en el que te han especificado perfectamente en el contrato que estás facultado a actuar como un actor malicioso, puedes buscar direcciones de dichas compañías, ver si alguna está comprometida y dónde.

Una vez averiguados los datos comprometidos, no se va a especificar concretamente todo lo que uno puede hacer con eso, pero es imaginable: localizar en la web oscura o similares la filtración, ver qué datos hay, si podemos sacar algo jugoso adicional (como un teléfono) o incluso una contraseña.

Y que si esta está en texto plano o con un *hash* débil… En fin, creo que se entiende. De esa manera, revelarías una importante vulnerabilidad OSINT para tu cliente.

Eso sí, mucho cuidado con tratar con fuentes de datos filtrados, tanto desde el punto de vista legal, como del técnico.

## 7\. OSINTGram, la mejor herramienta OSINT para cuentas de Instagram

![La herramienta OSINTGram](https://odint.net/images/osintgram.webp)

Las cuentas de Instagram están tan extendidas que es raro estar involucrado en una investigación OSINT y no tratar con ellas. Para facilitarnos la tarea está , probablemente, **la mejor herramienta OSINT para Instagram**.

Algunas de las cosas que podemos hacer con OSINTGram:

- **Obtener los seguidores** para buscar en ellos posibles nombres de usuario de interés de manera tranquila y eficiente (mucho mejor que en la web).
- **Descargar las fotos** a una carpeta.
- **Descargar usuarios** que el objetivo ha etiquetado.
- Descargar quién ha comentado en las fotos del usuario.

Y muchísimo más.

Para encontrar grados de relación, o buscar eficazmente entre multitud de datos de Instagram, OSINTGram es la respuesta.

## 8\. TwOSINT, la mejor herramienta OSINT para Twitter

![La herramienta OSINT para Twitter TwOSINT](https://odint.net/images/twosint.webp)

Dejamos Instagram para aterrizar en Twitter, hogar de la educación y el buen rollo. En este caso, **la mejor herramienta OSINT para analizar cuentas de Twitter es** .

TwOSINT es una aplicación OSINT compuesta de módulos, un poco **al estilo Metasploit**. Una vez la ejecutamos en la terminal de nuestra máquina virtual OSINT, podremos usar cada uno de sus 11 módulos, dependiendo de nuestro objetivo.

Desde conseguir información sobre los seguidores del objetivo con el módulo *followHunter*, hasta tratar de geolocalizar con el módulo *geoLocater*, TwOSINT ofrece multitud de opciones para encontrar esa información que deseamos del una cuenta de Twitter.

## 9\. Los operadores de búsqueda avanzados de Twitter

No abandonamos Twitter, porque si necesitamos buscar información en esa red, **los operadores avanzados de búsqueda de Twitter son un pequeño tesoro**.

Usándolos, al estilo *Google Dorking*, podremos filtrar y encontrar lo que deseemos en el mar interminable de *tweets*.

La propia red Twitter tiene una sin necesidad de estar aprendiendo los parámetros, como from: etc.

## 10\. Fisherman, herramienta OSINT para Facebook

Todo el que se haya encontrado con una tarea OSINT y Facebook sabe que **es la red más picajosa**. Debido a sus filtrados de datos y a la mina que es, muchos trucos y técnicas OSINT para Facebook que funcionan hoy, dejan de hacerlo mañana. Es una frenética carrera por tapar agujeros.

Del mismo modo y por experiencia, **no hay herramientas equivalentes a las que hemos visto para Twitter e Instagram** que merezcan la pena. No obstante, puede ser una buena aplicación para recoger información pública del objetivo, tenerla en local y examinarla con calma.

De todas maneras, lo ideal es **ir buscando en la propia red e ir conociendo esas técnicas, parámetros y maneras de sacar fotografías, amigos en común**, etc.

## 11\. Recon-NG, suite OSINT para reconocimiento de objetivos web

![](https://www.youtube.com/watch?v=n_D7hMLte48)

Recon-NG es obra de los magos de Black Hills y una herramienta OSINT veterana e **imprescindible cuando tenemos que hacer un reconocimiento pasivo de un objetivo web**.

Funciona, una vez más, de manera similar a Metasploit. Ejecutamos en terminal y **tendremos una serie de comandos y módulos que cargar y ejecutar** para conseguir información sobre el objetivo.

Datos del servidor, descubrimiento de *hosts*, subdominios o archivos interesantes son algunos de los muchos datos que podemos obtener de una web objetivo con Recon-NG.

Eso sí, requiere aprendizaje de su funcionamiento y saber qué estás haciendo y qué estás tratando de obtener.

## 12\. The Wayback Machine en Archive.org

![The Wayback Machine, una de las mejores herramientas OSINT](https://odint.net/images/wayback.webp)

Imposible no nombrar a Archive.org y, especialmente, **, entre las mejores herramientas OSINT**.

Allí, podremos analizar la historia de un sitio web y ver las copias antiguas que ha guardado esa máquina del tiempo.

¿El sitio está borrado? Probablemente, puedas encontrar qué ponía allí. ¿El sitio ha cambiado textos recientemente? Probablemente, puedas encontrar qué había antes.

Pocos trabajos no han hecho una o varias visitas a esta fenomenal herramienta OSINT.

## 13\. Wappalyzer, analiza qué tecnología usa una web

![La web de Wappalyzer](https://odint.net/images/wappalyzer.webp)

Esta es otra de esas herramientas imprescindibles en OSINT, cuando una web es el objetivo o está entre los datos de los que disponemos.

es una extensión de navegador para o para que nos permitirá, cuando estemos en una web, **saber qué tecnología está usando con solo hacer clic** en el icono de dicha extensión.

Así, nos dirá si utiliza Wordpress, el tipo de servidor, etc. De ahí se pueden extraer cosas muy interesantes.

También puedes buscar directamente en su web sin instalar nada.

## 14\. Hunter.io encuentra y valida emails

![Hunter, herramienta OSINT para encontrar y validar emails](https://odint.net/images/hunter.webp)

He aquí uno de esos ejemplos en los que herramientas comerciales de marketing superan ampliamente en efectividad a herramientas específicas OSINT.

es **un servicio que permite encontrar emails en dominios, validar si existe una dirección de correo y mucho más**. Hay multitud de herramientas de este tipo, Hunter sigue siendo la mejor, al menos por experiencia personal.

De verdad que, a la hora de encontrar gente y correos, las herramientas comerciales de marketing están a años luz. Especialmente, cuando se trata de extraer información de LinkedIn, hay algunas que resultan hasta demasiado inquietantes.

## 15\. Maltego. Uno de los programas OSINT más conocidos

![Maltego, la suite OSINT más famosa](https://odint.net/images/maltego.webp)

debe estar por méritos propios y es **una de las herramientas más famosas, completas y complejas** para investigaciones. Permite encontrar datos, establecer relaciones, organizar todo… pero he aquí una confesión.

No me ha parecido que merezca la pena aprenderlo a fondo o he extraído demasiado valor al usarlo. Una opinión **totalmente personal e intransferible**

Pero otros son fans declarados y dirían que el párrafo de arriba es un sacrilegio y es falta de entrenamiento en la herramienta. Eso es genial y no lo dudo, demuestra que, efectivamente, cada investigador tiene unas maneras, unos objetivos y unas herramientas preferidas.

Por eso, estas 15 (14 más bien, si quitamos Maltego) son las que, a día de hoy, resultan imprescindibles en lo personal cuando durante las labores OSINT de ciberinteligencia.

Hay más, muchas más instaladas y configuradas en las máquinas virtuales, pero, de veras que **un investigador avezado, usando Google y un navegador, puede sacar mucho más** que muchos con todas las herramientas OSINT del mundo.