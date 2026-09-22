# Lo primero a tener en cuenta en el diseño de una red es el alcance que esta tendra y recursos economicos disponibles. En mi caso, crear una nube privada capaz de brindarme un espacio de trabajo flexible, robusto y facil de escalar.

Conectividad IP y Seguridad de la Red

He contemplado un Fortigate 60E por varias razones como que es una de las marcas mejor posicionadas a nivel global en temas de firewall gracias a que disponen de producto de excelente calidad, existe muchisima documentacion, soporte nativo para el despliegue de VPN tanto Site-To-Site
como de acceso remoto, SD-WAN, inspeccion profunda de paquetes y se pueden encontrar de forma muy economica en el mercado de segunda mano (Dependiendo que tan critico es el proyecto, esto podria ser un riesgo de seguridad). 

Acceso a la red

Cisco Switch SG350-28P ofrece 24 puertos Gigabit Poe + 2 puertos SFP a 2 Gigabit + 2 puertos Gigabit T/SFP. Es un equipo de uso empresarial y al similar al fortigate, es un equipo de calidad y ampliamente documentado. Una decision de diseño a cuestionar es ¿ porque no elegir un FortiSwitch ?
La razon es que quiero diseñar una red Multi-Vendor y no depender unicamente de una compañia para toda la red.

Servidor

Para este asunto dispuse de mi vieja PC con las siguientes specs, cual he eliminado la gpu y la refrigeracion por agua para tener una eficiencia energetica lo mejor posible.
i5 11600 2.7GhZ 6 nucleos a 12 hilos
32 GB DDR4 3200 Mhz
NVDIA RTX2060
NZXT KRAKEN WATER PUMP
512 GB NVME a 3GB/S
EVGA 650W GOLD 



