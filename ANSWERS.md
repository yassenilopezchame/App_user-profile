# ANSWERS — Task 3

1. **¿Qué hace la visible propulsión Modal y por qué la controlamos con useState?** controla si el modal se renderiza en pantalla. Lo usamos con useState para poder abrirlo y cerrarlo desde la app (botón, backdrop, onRequestClose) sin desmontar el componente padre.

2. **¿Para qué sirve onRequestClose? ¿Qué ocurre en Android si no se cierra la ventana modal?** es el callback que se ejecuta cuando el usuario intenta cerrar el modal (botón back de Android, gesto). Si no se cierra el modal ahí, en Android el back no lo cierra y se queda abierto.

3. **¿Cuál es el efecto de transparent={true}? Nombra los tres valores de animationType** hace que el fondo del Modal sea transparente, permitiendo ver la pantalla detrás. Los tres valores de animationType son: `none`, `slide` y `fade`.

4. **¿Por qué ScrollView existe? ¿Qué sucede con un largo View sin él? ¿Cuándo elegirías FlatList en su lugar?** permite desplazar contenido que no cabe en pantalla; sin él un View largo se recorta y no se puede ver. Elegiría `FlatList` cuando la lista es larga o dinámica, porque virtualiza y renderiza solo lo visible.

5. **¿Cuál es la diferencia entre los style y los contentContainerStyle accesorios de un ScrollView?** `style` aplica al contenedor externo del ScrollView (tamaño, márgenes, maxHeight); `contentContainerStyle` aplica al View interno que envuelve el contenido (padding, gap, alineación).

6. **¿Para qué sirve SafeAreaView y qué zonas del dispositivo protege? ¿Por qué lo usamos react-native-safe-area-context?** SafeAreaView protege el contenido de los recortes del notch, la isla dinámica y las barras del sistema (status bar y barra inferior). Usamos `react-native-safe-area-context` porque es la librería recomendada en Expo y funciona igual en iOS y Android.

7. **Describe con tus propias palabras las tres mejores prácticas de la lista de verificación del Paso 5 y da un ejemplo de cuándo no es buena idea usar una ventana modal** 
* usar un solo modal por pantalla para acciones cortas y enfocadas 
* limitar el contenido de los ScrollView 
* envolver la pantalla en SafeAreaView 

Un modal no es buena idea para mostrar contenido largo o navegación principal.