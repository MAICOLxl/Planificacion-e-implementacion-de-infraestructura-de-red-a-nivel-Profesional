##El caso que mencionas es fascinante y, de hecho, se trata del famoso Robo al Banco Central de Bangladesh en 2016, donde el grupo norcoreano Lazarus Group intentó robar 951 millones de dólares y logró desviar inicialmente 101 millones (81 millones a Filipinas y 20 millones a una cuenta en Sri Lanka).
Para responder a tu pregunta: fue una mezcla perfecta de ambos factores (humano y técnico), ejecutada con una paciencia y precisión militar. Los atacantes no rompieron el cifrado de la red financiera global (SWIFT), sino que hackearon el entorno local del banco combinando ingeniería social con negligencia técnica extrema.
Así es como burlaron la seguridad paso a paso:
1. El Factor Humano: La Puerta de Entrada (Phishing)
El ataque comenzó casi un año antes del robo. Los hackers enviaron correos electrónicos falsos de Phishing dirigido (Spear-phishing) a varios empleados del banco de Bangladesh, haciéndose pasar por solicitantes de empleo que adjuntaban su currículum.
• Un empleado cayó en la trampa y abrió el archivo adjunto.
• Al hacerlo, descargó silenciosamente un malware de acceso remoto (troyano) en la red interna del banco.
2. El Factor Técnico: Negligencia Extrema en la Red
Una vez dentro de la red, los hackers descubrieron un panorama técnico desastroso que les facilitó todo:
• El banco utilizaba switches de red baratos de 10 dólares (no administrables) en lugar de switches profesionales.
• No había segmentación de red: La red de las computadoras de la oficina (donde leían correos) estaba conectada directamente y sin defensas a la red ultra secreta de las terminales de SWIFT (el sistema internacional para transferir millones de dólares). No había un firewall como el FortiGate bloqueando los saltos laterales.
• Los hackers instalaron keyloggers (registradores de teclas) para robar las credenciales de los operadores que tenían autorización de transferir dinero.
3. El Factor Estratégico (El Factor Humano a nivel Macro)
Los norcoreanos estudiaron los hábitos del personal y el calendario mundial. Lanzaron el ataque un jueves por la noche.
• El viernes es el día de descanso en el mundo islámico (Bangladesh cerrado).
• El sábado y domingo es el fin de semana en Nueva York (donde la Reserva Federal procesaba los pagos).
• El lunes era el Año Nuevo Chino (Filipinas cerrado, donde se lavaría el dinero).
Aprovecharon la desconexión humana de los fines de semana para que nadie pudiera llamarse por teléfono para confirmar las transferencias sospechosas.
¿Cómo enviaron el dinero a Sri Lanka?
Los hackers usaron las credenciales legítimas robadas para ordenar a la Reserva Federal de Nueva York que enviara el dinero. Enviaron 35 órdenes de transferencia. Cuatro pasaron limpias a Filipinas, y una de 20 millones de dólares fue enviada a una ONG en Sri Lanka.
El error que los salvó del billón de dólares
El ataque entero se cayó por un error humano de los propios hackers: en la transferencia a Sri Lanka, escribieron mal la palabra "Foundation" (Fundación) y pusieron "Fundation". Un banco intermediario vio la falta de ortografía, le pareció sospechoso, detuvo las transferencias restantes (salvando 850 millones) y la alerta saltó en todo el mundo. Los 20 millones enviados a Sri Lanka se congelaron y se recuperaron por completo.
La lección para tu laboratorio
Este caso real respalda perfectamente lo que hablábamos del FortiGate y OpenProject: el sistema de cifrado de la Reserva Federal y de SWIFT era inquebrantable (como la Fase 1 y Fase 2 de IPsec), pero los hackers entraron por el eslabón débil (el correo de un empleado) y se movieron libremente porque el banco no tenía segmentada su red interna.
Por eso es tan valioso lo que estás haciendo con tu FortiGate: al aislar tu OpenProject y no dejar la red en "ALL", estás impidiendo matemáticamente que un error humano en tu PC personal comprometa tu servidor de proyectos.
