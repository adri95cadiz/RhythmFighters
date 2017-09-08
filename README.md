# RhythmFighters
Fighting and Rhythm game prototype developed in UE4 for Universidad de Granada.

Rhythm Fighters es un nuevo concepto de juego que trata de unificar un juego de lucha y un juego de ritmo, adaptado a los dispositivos móviles táctiles actuales. Aunque actualmente está en fase de prototipo, la idea concebida es un juego frenético con infinidad de posibilidades debido a que podríamos introducir nuestra propia música y el juego se ajustaría a ella. Aunque actualmente esto no está implementado, sería así en la versión final y en la idea original del juego, así como modos competitivos online y locales por bluetooth.

El juego como está actualmente consta de dos personajes, uno controlado por el jugador y otro por la IA que luchan en un escenario siguiendo el ritmo de la música. Entre sus particularidades se encuentra que toda acción realizada por el jugador debe ser realizada al ritmo de la música (barra de ritmo), y que su eficacia dependerá de la precisión del toque, haciendo el combate simultaneo pero manteniendo el jugador al límite constantemente.

Ambos jugadores constan de 8 movimientos posibles:
- Movimiento:    
    - Derecha - Izquierda
    - Salto - Descenso
    - Salto Izquierda - Salto Derecha
- Lucha:
    - Atacar
    - Defender

En el combate el jugador si defiende bloqueará todo el daño, sin embargo si ataca el daño será su daño menos el daño del oponente, recibiendo daño aquel que fue menos preciso en el ritmo. Si los jugadores no se encuentran lo bastante cerca el ataque resultará inservible, como es lógico, ya que no golpeará.

Una mejora sería que cuando los oponentes se dirijan a la misma posición se encuentren en un duelo que gane el más preciso en el siguiente movimiento.

Instrucciones para jugar.

Rhythm Fighters está desarrollado en Unreal Engine 4, actualmente tengo compilada la versión para Windows, sin embargo, el juego está pensado para dispositivos táctiles tipo Android y otros, por tanto si lo continúo los smartphones actuales serán su plataforma principal.

No es necesaria ninguna libreria ni instalación especial para jugar Rhythm Fighters, solamente descargarlo y lanzarlo, puesto que está programado con las funciones nativas del motor.

Tutorial.

El juego es muy simple, consta de una interfaz radial en la cual se pueden apreciar las diferentes acciones antes mencionadas, en forma de botones, estos deberán ser pulsados cuando la barra inferior al personaje alcance la primera raya roja (en su 80\%), a partir de entonces el movimiento será efectuado correctamente. Además, el ataque será más fuerte cuanto más progreso haya alcanzado la barra inferior de ritmo, si no se ejecuta el movimiento en ritmo, el personaje quedará bloqueado hasta el siguiente movimiento.

Siguiendo estas mecánicas y siendo hábil y lo bastante estratégico, tendremos que ganar a nuestro oponente eliminando su barra de vida al golpear en el momento justo, de esa forma ganaremos la partida.

Diseño del juego.

En su apartado gráfico es donde el juego se encuentra en un estado más primitivo, sus assets son reciclados de páginas de uso libre y el contenido estándar de UE4, esto es así porque no dispongo de las capacidades artísticas necesarias para un buen desarrollo gráfico del juego.

Por otro lado, hablando del diseño del juego como algo más conceptual, los diseños previos difieren bastante de la versión actual, sin embargo una idealizada versión final seguiría mis diseños iniciales (los cuales se encuentran en las dos carillas de un folio), casi a rajatabla. El juego especialmente en su interfaz y apartado gráfico difiere mucho de la idea original, aunque en concepto se asemeja lo suficiente a mi idea como para poder ser un prototipo digno de muestra.

Al haber sido realizado en Unreal Engine no he necesitado un diseño preliminar del tipo Requisitos, Diagrama de Clases, etc. ya que Unreal facilita mucho todas esas tareas.

Inteligencia Artificial.

En principio la IA del juego iba a estar contenida en un árbol de comportamiento de unreal, pero ya que por como estaba implementada la lógica del personaje y sus acciones esto no era posible, esto fue finalmente descartado, y la IA se implementó finalmente en el blueprint del personaje controlado por la IA.

Básicamente la IA se dedica a acercarse al jugador hasta tenerlo a rango de ataque y una vez en rango de ataque, defender si prevé un ataque del rival o atacar con la mayor precisión posible, su punto débil sería hacer ataques altamente precisos aunque arriesgando perderlos, pero de esta forma la IA no podría reaccionar a tiempo y no podría defenderse de ellos, aunque aún así hay que tener cuidado ya que la IA es extremadamente precisa (+90% casi todos los casos).

Otro truco para ganar a la IA fácilmente, aunque lo consideraría exploit de la poca capacidad de razonamiento de la IA, sería hacerla caerse confundiéndola a base de moverse mucho hasta que finalmente cayera por el borde de alguna plataforma.

Trabajo futuro y posibles mejoras.

Pretendo en el futuro continuar este proyecto o adaptar sus ideas a otros, ya que me parece una idea entretenida y con cierta posibilidad de éxito si se pule lo suficiente.

Algunas posibles mejoras para el juego serían:

- Feedback en pantalla de aciertos, errores, y la precisión de los aciertos.
- Feedback en pantalla de los daños realizados y recibidos en un golpe.
- Efectos de particulas al atacar, defender y golpear, así como sus correspondientes efectos de sonido.
- Estado de victoria o derrota al terminar la partida (actualmente la barra de vida termina pero el juego continua).
- Mejora del movimiento por las plataformas, actualmente es algo impreciso y a veces las físicas juegan malas pasadas.
- Implementación de ataques especiales y el modo "Frenzy" en el cual el ritmo se elimina y los jugadores pueden efectuar tantos movimientos como quieran sin casi restricción.
- Mejoras visuales para el ritmo y para el juego en general.
- Inclusión de nuevos mapas y personajes.
- Mayor número de mecanicas e interacciones entre ellas (más profundidad en el sistema de combate, aunque los controles se mantengan igual), por ejemplo con combos aéreos.
