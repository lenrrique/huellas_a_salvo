# huellas_a_salvo
¿DE QUÉ SE TRATA?
“Huellas a Salvo” es el nombre de esta revista interactiva de carácter informativo que pretende compartir conocimientos acerca de los perros a través de cinco secciones: razas, nutrición, salud, abandono (centrando esta problemática en la ciudad de Camoapa), y seguridad. Además de eso, podrás encontrar links que te redirigirán a una producción audiovisual sobre este tema y a nuestro portafolio digital, que contiene todo el material que producimos para esta campaña de concienciación.
Nuestro objetivo es sensibilizar a la sociedad, sobre la importancia que tiene el brindarles una vida digna a los caninos en general, y, sobre todo, de darles una oportunidad a los perros abandonados, que también merecen ser tratados condescendientemente, como los seres vivos extraordinarios que son.
ESTRUCTURA DE LA WEB
Para construir esta revista interactiva utilizamos los archivos html, css, java script y json, que contienen los códigos pertinentes que le brindan la estructura, la apariencia y la funcionalidad necesarias para marchar correctamente.
Primeramente, en el archivo HTML, estructuramos y desplegamos el contenido de la página web. Este contiene el título de la misma y todos los elementos primordiales, como el favicon, el logo del proyecto y los id que enlazarán los contenedores de información con los demás archivos. A continuación, mostramos los códigos correspondientes al HTML.

<!DOCTYPE html>
<html>
<head>
 <title>Huellas a Salvo</title>
 <link rel="stylesheet" type="text/css" href="estilos.css">
 <link rel="icon" type="image/vnd.icon" href="imagenes/favicon.ico">
</head>
<body>
    <img class="logo" src="imagenes/logo.png" alt="" width=20px>
 <h1 id="revista-titulo"></h1>
 <div id="articulos-container"></div>
 <div id="modal" class="modal">
 <div class="modal-content">
 <span class="close">&times;</span>
 <h2 id="modal-titulo"></h2>
 <img id="modal-imagen1" src="" alt="" class="modal-imagen">
      <p id="modal-contenido"></p>
      <img id="modal-imagen2" src="" alt="" class="modal-imagen">
    </div>
  </div>
  <a href="https://vm.tiktok.com/ZM2CaFq6H/" class="button">VIDEO</a>
  <a href="https://sites.google.com/view/huellasasalvo/home" class="button2">PORTAFOLIO</a>
  <a href="https://drive.google.com/file/d/19qODTDKnu7Z3QCeb0re90tpDqNmsD06Z/view?usp=sharing" class="button3">Continua leyendo: Campaña de Adopción Canina</a>
  <script src="app.js"></script>
</body>
</html>

Seguidamente, en el archivo CSS ordenamos todas las instrucciones referentes a la apariencia del sitio para así presentar el contenido de la página de forma atractiva. Aquí configuramos el tamaño y la disposición tanto de la imagen de fondo, como del logotipo, pero también disponemos el color y tipografía de cada uno de los textos, así como la apariencia de los contenedores de información y lo que llevan dentro.
Con respecto a la imagen de fondo, esta tiene un tamaño de 1340 px, mientras el logotipo mide 500px. La tipografía utilizada para todos los textos es Arial, perteneciente a la familia tipográfica de las san-serif. Los colores corporativos no fueron utilizados para las tarjetas, ya que la imagen de fondo le brinda el color suficiente a la apariencia de la web. El favicon utilizado corresponde a la manera más simplificada a la que puede llegar nuestro logotipo, mostrando solo la huella canina. Las imágenes que se encuentran dentro de cada una de las tarjetas tienen un ancho de 500px y están alineadas al centro. El texto de las mismas, se divide en tres artículos por sección, y se encuentran de manera justificada. Aquí puedes ver los códigos que utilizamos en el CSS.
body {
    position: relative;
   }
   .logo{width: 500px;
      text-align: center;
      margin-left: 32%;
      padding: 0;
      margin-top: 0;}
   body::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 200%;
    height: 200%;
    background-image: url('imagenes/fondo.jpg');
    background-size: 1340px;
    opacity: 1;
   
    /* Ajusta el valor de la opacidad (0.7 en este caso) */
    z-index: -1;
   }
   h1 {
   font-family: Arial, Helvetica, sans-serif;
   color: white;
    padding: 20px 0;
    margin-left: 26%;
    margin-top: 0;
    padding-top: 0;
   }
   #articulos-container {
      font-family: Arial, Helvetica, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    padding: 20px;
   }
   .articulo-card {
   font-family: Arial, Helvetica, sans-serif;
    flex-basis: 300px;
    flex-grow: 1;
    padding: 20px;
    margin: 10px;
    background-color: #e4e4e4;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
   }
   .articulo-card:hover {
    transform: translateY(-5px);
    cursor: pointer;
   }
   .articulo-card h3 {
      font-family: Arial, Helvetica, sans-serif;
    margin-top: 0;
   }
   .articulo-card img {
    width: 100%;
    height: auto;
    margin-bottom: 10px;
   }
   .articulo-card p {
      font-family: Arial, Helvetica, sans-serif;
    margin-bottom: 0;
   }
   /* Estilos para el modal */
   .modal {
      font-family: Arial, Helvetica, sans-serif;
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.4);
   }
   .modal-content {
    background-color: #e4e4e4;
    margin: 0 auto 0 auto;
    /* Ajustamos los márgenes */
    padding: 20px;
    border: 1px solid #888;
    width: auto;
    max-width: 60%;
    box-sizing: border-box;
    text-align: center;
    overflow: auto;
    border-radius: 10px;
    border: 2px dashed black;
   }
   .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
   }
   .close:hover,
   .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
   }
   .modal-imagen {
    display: block;
    width: 500px;
    height: auto;
    max-width: 100%;
    max-height: 100%;
    margin: 20px auto;
    object-fit: contain;
   }
   #modal-contenido {
    line-height: 1.5;
    text-align: justify;
   }
   @media screen and (max-width: 600px) {
    .modal-content {
    margin: 20px;
    padding: 10px;
    width: auto;
    max-width: none;
    border-radius: 10px;
    }
    .modal-imagen {
    max-width: 100%;
    }
   }
   .modal-abierto {
    animation: abrirModal 0.2s ease-out;
   }
   @keyframes abrirModal {
    0% {
    opacity: 0.2;
    transform: scale(2.3);
    }
    100% {
    opacity: 1;
    transform: scale(1.2);
    }
   }
   .modal-cerrado {
    animation: cerrarModal 0.3s ease;
   }
   @keyframes cerrarModal {
    0% {
    opacity: 1;
    transform: scale(1);
    }
    80% {
    opacity: 0;
    transform: scale(3);
    }
    100% {
    opacity: 0;
    transform: scale(2);
    }
   }
   .button {
      display: inline-block;
      font-family: Arial, Helvetica, sans-serif;
      padding: 10px 20px;
      background-color: #1f27bf;
      color: white;
      text-decoration: none;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      margin-left: 30px;
   }
   .button2 {
      display: inline-block;
      font-family: Arial, Helvetica, sans-serif;
      padding: 10px 20px;
      background-color: #1f27bf;
      color: white;
      text-decoration: none;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      margin-left: 30px;
   }
   .button3 {
      display: inline-block;
      font-family: Arial, Helvetica, sans-serif;
      padding: 10px 20px;
      background-color: #9b6213;
      color: white;
      text-decoration: none;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      margin-left: 30px;
   }

Por otro lado, en el archivo JAVA SCRIPT añadimos la interactividad y las funciones que mejorarán la experiencia del usuario que visite nuestra web. Este archivo va incrustado en el html al igual que el anterior, el css. Por acá les dejamos los códigos que le brindan a nuestra web sus respectivas funcionalidades.

fetch('data.json')
  .then(response => response.json())
  .then(data => {
    const revistaTitulo = document.getElementById('revista-titulo');
    const articulosContainer = document.getElementById('articulos-container');
    revistaTitulo.textContent = data.titulo;

    data.articulos.forEach(articulo => {
      const articuloCard = document.createElement('div');
      articuloCard.classList.add('articulo-card');
      articuloCard.innerHTML = `
        <h3>${articulo.titulo}</h3>
        <img src="${articulo.imagen1}" alt="">
        <p>${limitarDescripcion(articulo.contenido, 10)}</p>
        <img src="${articulo.imagen2}" alt="">

      `;
      articuloCard.addEventListener('click', () => {
        mostrarModal(articulo);
      });

      articulosContainer.appendChild(articuloCard);
    });

    const imagenes = document.querySelectorAll('.articulo-card img');
    imagenes.forEach(function (imagen) {
      imagen.style.display = 'none'; // Oculta todas las imágenes al cargar la página
    });
  })
  .catch(error => {
    console.log('Error al cargar el archivo JSON:', error);
  });

function limitarDescripcion(texto, longitud) {
  const palabras = texto.split(' ');
  if (palabras.length > longitud) {
    return palabras.slice(0, longitud).join(' ') + '...' + '<br><br>Seguir leyendo...';
  }
  return texto;
}

function mostrarModal(articulo) {
  const modal = document.getElementById('modal');
  const modalTitulo = document.getElementById('modal-titulo');
  const modalImagen1 = document.getElementById('modal-imagen1');
  const modalContenido = document.getElementById('modal-contenido');
  const modalImagen2 = document.getElementById('modal-imagen2');

  modalTitulo.textContent = articulo.titulo;
  modalContenido.innerHTML = articulo.contenido.replace(/\n/g, '<br>');
  modalContenido.classList.add('modal-abierto');

  modal.style.display = 'block';

  modalImagen1.style.display = 'none'; // Oculta la imagen inicialmente
  modalImagen2.style.display = 'none'; // Oculta la imagen inicialmente

  modalImagen1.onload = function () {
    modalImagen1.style.display = 'block'; // Muestra la imagen cuando se carga
  };

  modalImagen1.src = articulo.imagen1;

  modalImagen2.onload = function () {
    modalImagen2.style.display = 'block'; // Muestra la imagen cuando se carga
  };
  modalImagen2.src = articulo.imagen2;

  const closeBtn = document.getElementsByClassName('close')[0];
  closeBtn.addEventListener('click', () => {
    modalContenido.classList.add('modal-cerrado');

    setTimeout(() => {
      modalContenido.classList.remove('modal-cerrado');
      modal.style.display = 'none';
    }, 300);
  });

  window.addEventListener('click', event => {
    if (event.target === modal) {
      modalContenido.classList.remove('modal-abierto');
      modal.style.display = 'none';
    }
  });
}

Por último, mediante el archivo JSON, pudimos estructurar todos los datos de la revista en forma de texto y así permitir el intercambio de información entre aplicaciones de manera sencilla, liviana y rápida. La manera en que fue estructurada fue a través de tarjetas, que corresponden cada una a cada sección de la revista. Al dar click en ellas se desplega la información e imágenes que cada una contiene. A continuación, mostramos los códigos correspondientes a este archivo.

{
    "titulo": "Una guía para la vida digna de los caninos",
    "articulos": [

    {
    "titulo": "INTRODUCCIÓN",
    "imagen1":"imagenes/introducción1.jpg",
    "contenido": "LA RESPONSABILIDAD DE TENER UN PERRO\n\nElegir un perro debería ser una decisión relevante en nuestra vida porque nos responsabilizamos de prestar cuidados a otro ser vivo. ¿Por qué le damos tanta importancia? Porque los cuidados hacia ellos deben darse durante todo el tiempo que él viva y porque se deben tener en cuenta muchos detalles: desde el tiempo que hay que dedicarles, hasta cuánto cuestan los cuidados de higiene y los cuidados veterinarios.\n\nEl compromiso de tener un perro debe asumirse tras realizar un análisis riguroso y honesto, nunca por un impulso momentáneo, al contrario, antes de tener un perro o cachorro debemos pensarlo bien para que no llegue el arrepentimiento. La responsabilidad de criar a un perro debe asumirse durante toda la vida del animal, por eso ponemos un énfasis muy especial en que el abandono de perros es una de la acciones más crueles e irresponsables. No sólo es injusto para el animal, sino que está prohibido por ley.\n\nAnte la detección de la problemática del abandono canino, decidimos crear Huellas a salvo, una revista de carácter informativo que pretende compartir conocimientos acerca de los perros a través de cinco secciones que comprenden: las razas existentes en el mundo actualmente, la manera correcta de alimentarlos, los posibles problemas de salud que puedan enfrentar y cómo resolverlo, el abandono al que son sometidos una gran cantidad de ellos, centrando esta problemática en la ciudad de Camoapa, y las alternativas de seguridad que podemos implementar para darles una vida más digna. \n\nEsto con el fin de sensibilizar a la sociedad, sobre la importancia que tiene el brindarles una vida digna a los caninos en general, y, sobre todo, de darles una oportunidad a los perros abandonados, que también merecen ser tratados de con condescendientemente como los seres vivos extraordinarios que son.",
    "imagen2":"imagenes/introduccion2.jpg"
    },
    {
    "titulo": "RAZAS",
    "imagen1": "imagenes/razas1.jpg",
    "contenido": "UNA GRAN DIVERSIDAD PARA UNA SOLA ESPECIE\n\n ¡El primer canino fue un lobo!\n\n Los perros nacen en el viejo mundo hace más de veinte mil años a partir de lobos, quienes en búsqueda de alimento comenzaron a acercarse a las aldeas de humanos, y eventualmente se fueron domesticando y evolucionando hasta convertirse en los perros que conocemos hoy en día.\n\n A lo largo de la historia, los humanos han ido seleccionando a los perros según las características que fueran necesarias para su función (caza, pastoreo, compañía, etc), generando así muchísimos tipos de perros diferentes.\n\n Para gustos los colores, muchas razas para tu compañero fiel\n\n Para conocer sobre las razas de perros, debemos saber que existen organizaciones internacionales que regulan las características de las razas y sus estándares; y son quienes determinan y reconocen la validez de las nuevas que surgen. La organización más importante es la Federación Cinológica Internacional, que reconoce alrededor de 350 razas oficiales, divididas en grupos, sin embargo, este número es muy dinámico y crece anualmente.\n\n El grupo de los perros de pastoreo, por ejemplo, incluye al Pastor Alemán o al Collie. Los perros de montaña, en cambio, comprenden razas como el Doberman, Rottweiler, Dogo o Gran Danés. En el grupo de los Terriers, se encuentra el Fox Terrier y el Bull Terrier. El de los Teckels, comprende a los perros salchicha en todas sus variedades. Razas como el Husky Siberiano, el Chow Chow o el Andino, se encuentran entre los perros primitivos. En cambio, los perros de rastro incluyen al Sabueso y al Dálmata. Entre los perros de muestra está el Pointer o el Braco Alemán, entre los perros levantadores de caza, el Labrador y el Retriver. Los perros de compañía incluyen al Poodle, Chihuahua, Pug o Pekinés, y los perros Lebreles, contienen al Galgo y el Saluki.\n\nNICARAGUA, UN PAÍS CON ABUNDANCIA CANINA\n\n¡Seguro podrás identificarlos!\n\nAhora que ya sabes que el número de razas existentes de caninos es muy grande, nos gustaría centrarnos principalmente en las que mayoritariamente abundan en Nicaragua. Según los datos propiciados por el hospital nicaragüense Veterinarios Asociados, la raza de los Dogo es una de las más comunes, que se caracteriza por ser fuerte y tener un gran agarre. Tiene una cabeza redonda y un cuerpo ancho, lo que le aporta una apariencia robusta. También se, el pelo corto y con frecuencia un color tipo beige.\n\nPor otro lado, de las razas que más encontramos en el país son los mestizos, que no tienen una raza en particular (al menos no una que sea reconocida de forma oficial), pero que surgen como resultado de la mezcla entre animales de razas diferentes. Debido a esto, las características físicas y de comportamiento en estos animales pueden variar significativamente.\n\nLos Terriers, que incluyen todas sus variaciones, también son de los que más abundan en Nicaragua. Los perros de este tipo se caracterizan por ser pequeños, con un pelo áspero y un carácter marcado por la determinación. Se trata de animales bastante enérgicos, que aman jugar y divertirse. En cambio, la raza Andina, originaria de Perú, tiene características muy diferentes, como la ausencia de pelo, sin mencionar que se trata de animales de gran tamaño, fuerza y determinación. Igualmente, muchas personas utilizan perros andinos como animales de compañía.\n\nFinalmente, la última raza de perros más común de la que nos gustaría hablarte son los Pitbull. Estos animales son extremadamente fuertes, resistentes e independientes. De igual manera, como ocurre en otros casos, también existen varias razas de perros Pitbull, y dependiendo del lugar donde te encuentres, en el país con toda seguridad podrás ver más un tipo.\n\nDESPRECIO INJUSTIFICADO HACIA LOS MESTIZOS\n\nUna vida lamentable e inmerecida \n\nEn nuestro país el abandono de los caninos es muy común, en especial cuando se trata de los perros mestizos. Para estos, la vida no suele ser nada buena, y por una u otra razón terminan viviendo en las calles, expuestos a peligros, incluso, en el proceso de reproducción, las crías que llegan a la vida, sufren las mismas condiciones que sus progenitores, enfrentándose a situaciones de vulnerabilidad debido a los peligros que corren.\n\nEstos perros carecen de comida, suelen alimentarse de basura o de desperdicios que las personas les dan, no cuentan con atención veterinaria y con frecuencia se encuentran en situaciones de alarma como heridas (causadas intencionalmente por las mismas personas que los consideran una plaga), laceraciones en la piel por garrapatas o pulgas, fracturas (a causa de accidentes de tráfico) o enfermedades terminales. \n\nMenospreciados sin motivos lógicos\n\nLa principal razón por la que esta raza de caninos es abandonada es porque son considerados “perros sin raza” o “perros machines”, además de ser vistos como sucios, feos o impuros por el simple hecho de que la mayoría de ellos nacen en las calles y en condiciones deplorables. Por otro lado, la necedad del ser humano de ver a las mascotas como mercancía o lujo, provoca que siempre quieran adquirir aquellas razas que cuestan muchísimo dinero, como si adoptar un perro mestizo significara “ser pobre”. \n\nSin embargo, la ironía de la situación es que pese a ser los más abandonados, un estudio realizado por investigadores del Departamento de Ciencia Animal de la Universidad de Sydney, el veterinario Paul McGreevy señala que “la salud genética que presentan estos perros es sustancialmente mayor a la de los de razas oficializadas”, y detalla que, “tienen una probabilidad mucho menor de manifestar trastornos o enfermedades.”",
    "imagen2": "imagenes/razas2.JPG"
    },
    {
    "titulo": "NUTRICIÓN",
    "imagen1": "imagenes/nutricion1.jpg",
    "contenido": "¡ALTO! NO SIGAS COMETIENDO ESTOS ERRORES\n\nEllos comerán todo lo que puedan \n\nCuidar de la alimentación canina es fundamental, puesto que los errores que cometemos al tratar de alimentarlos, posteriormente pueden costarles mucho sufrimiento. Para el nutricionista canino Oliver Klowkowski, uno de los errores más comunes es el suministro de energía excesiva, que provoca que estos sufran cada vez más de obesidad y todas sus consecuencias. El problema es que el perro no se detendrá una vez que se sienta lleno. En cambio, él (como su pariente lobo) comerá tanto como pueda, puesto que no sabe cuándo obtendrá algo nuevamente.\n\nOtro problema que está relacionado con un suministro de energía excesivo, es la administración adicional de snacks procesados. Si le das a tu perro snacks en exageración, tarde o temprano se volverán notorias en forma de sobrepeso a pesar de la cantidad correcta de alimentos. Esto aplica aún más si el canino no realiza suficiente movimiento. \n\nCuida a tu amigo evitando estos alimentos \n\nEl mismo profesional también advierte sobre el uso de aceite adicional sobre la comida de las mascotas, puesto que suelen causar cantidades sorprendentes de heces y diarrea. La comida para perros suele ser un alimento completo, así que, si le proporciona la cantidad adecuada, automáticamente se le suministrarán suficientes proteínas, carbohidratos y grasas.\n\nAlgunos alimentos, como el chocolate, las uvas o el aguacate pueden dañarlos gravemente, por lo tanto, hay que evitarlos como recompensas. La comida para perros también puede dañarse, así que, si el saco de concentrado ha estado abierto durante meses y todavía no se ha agotado, puede ser hora de deshacerse de él y comprar nueva comida. Debes tener en cuenta que algunos productos también son infecciosos. Estos incluyen, por ejemplo, orejas de cerdo y guisantes, que pueden causar problemas digestivos en su perro.\n\n UN AJUSTE ALIMENTARIO PARA CADA ETAPA DE SU VIDA\n\n Conforme crezcan comerán diferente \n\n“Los alimentos se rigen a la etapa de vida de tu mascota”, estas son las palabras de Alejandro Martínez, educador y adiestrador canino, así mismo, señala que, en el caso de los cachorros, que están en crecimiento acelerado y constante es indispensable una buena alimentación, porque debe cumplir y abastecer de forma continua su veloz desarrollo.\n\n En los adultos es diferente, ya que su actividad es menor al igual que su energía. Es importante darle la alimentación adecuada, ya que el alimento para cachorros puede volver a tu perro adulto, obeso. Un perro de 7 años debe tener una dieta con gran cantidad de antioxidantes, proteína de calidad, grasas y carbohidratos más bajos. \n\nEn el senior pasa lo mismo, al igual que los perros adultos un perro senior puede engordar rápidamente si no tiene la alimentación adecuada y las porciones medidas, ya que todo se transforma en grasa y difícilmente un perro mayor puede quemarla. También hay que tener en cuenta que una dieta basada en alto nivel de proteína puede afectar el riñón y generar graves complicaciones a futuro. Su alimentación debe estar basada en bajos carbohidratos, más antioxidantes.\n\nCategorizar los alimentos también es importante\n\n En cuanto a categorías de alimentos, el experto expone que las más conocidas son las de combate (categorías básicas), las premium con buena calidad y las súper premium con una calidad supremamente alta. De la misma manera, recomienda que la alimentación que le brindes a tu perro debe ajustarse al estilo de vida que lleva, pero también a tus recursos disponibles. Sin embargo, evita a medida de tus posibilidades, no dar aquellos alimentos de “combate’’ a tus perros, ya que su composición es cuestionable al no tener muchos controles de calidad.\n\nSI ALIMENTAS A UN PERRO ABANDONADO ¡PRESTA ATENCIÓN!\n\n La desnutrición será notable\n\nSi ves por las calles a un perro callejero, probablemente esté en estado de desnutrición, con poco peso y con alguna afectación en su sistema digestivo (ya que estos pobres canes suelen alimentarse de lo que sea que encuentren en los desperdicios, por lo tanto, seguramente has considerado alimentarlos con el fin de que se encuentren mejor. Estamos convencidos de que podemos ayudarte a conseguir la recuperación de un perro desnutrido y desmontar creencias erróneas que puedas tener en relación a este tema. \n\nLa solución no está en la cantidad\n\nDesgraciadamente, con frecuencia se encuentran muchísimos perros en la calle, e intentamos ayudarlo alimentándolo de manera que se le ofrece una gran cantidad de concentrado o comida, creyendo que así se recuperará rápidamente de su hambre y su estado físico. \n\nLa investigadora Yesica Flores, que también es autora del blog “Conociendo a mi perro”, nos informa acerca del error que cometemos al alimentar en abundancia a un animal moribundo, pero ¿por qué es tan grave?\n\nPues la respuesta es sencilla. Cualquier perro que no esté habituado a obtener comida regularmente puede sufrir enormes problemas si le damos alimentación excesiva de golpe, dado que su sistema digestivo no está acostumbrado a ese tipo de ingestas. Problemas como variaciones excesivas de los niveles de fósforo y potasio pueden causar un desorden interno severo en los caninos.\n\nNuestra recomendación si quieres alimentar a un perro callejero, es que le brindes porciones pequeñas. De esta manera le estarás ayudando a nutrirse mejor, pero también cuidarás de su bienestar. Y en el caso de que decidas alimentarlo periódicamente o adoptarlo como mascota, ve incrementando poco a poco las cantidades, de manera que el canino se vaya acostumbrando de manera progresiva a su nueva dieta.",
    "imagen2":"imagenes/nutricion2.jpg"
    },
    {
    "titulo": "SALUD",
    "imagen1": "imagenes/salud1.jpg",
    "contenido": "CUIDA A TU COMPAÑERO COMO SE LO MERECE\n\nUn plan de vacunación para una mejor calidad de vida\n\nCumplir con la pauta de vacunación recomendada por las organizaciones veterinarias es fundamental para garantizar la salud y el bienestar de nuestros perros. Las vacunas protegen no sólo a nuestras mascotas, sino que también contribuyen a evitar la propagación de enfermedades, tanto entre otros perros como en otras especies, incluidos nosotros, los humanos. \n\nSon fundamentales para prevenir la aparición de enfermedades infecciosas y conseguir un sistema inmunológico fuerte que prevenga la aparición y diseminación de enfermedades. \n\nSegún las recomendaciones oficiales de World Small Animal Veterinary Association (WSAVA), la primera vacuna se les aplica a los cachorros entre las 6 y las 9 semanas, y se administra una vacuna monovalente (solo parvovirus) o bivalente (parvovirus y moquillo). Luego, entre las 3 y 4 semanas después de la primera dosis, se pone una segunda vacuna, esta vez añadiendo protección hacia enfermedades adicionales (como leptospirosis). Por esta razón la llamamos vacuna polivalente.\n\nEntre 3 y 4 semanas después de la segunda dosis se pone una nueva dosis de vacuna polivalente. Y, por último, debe aplicarse la vacuna antirrábica, obligatoria por ley en muchas comunidades, y que, además, es obligatoria para viajes internacionales.\n\nEn la actualidad es esencial realizar recordatorios de la vacuna polivalente y de la rabia en perros adultos. La mejor forma de estar al día del calendario de vacunación de nuestro perro es acudiendo al veterinario. \n\nPara que nuestra mascota viva en las mejores condiciones es necesario prevenir cualquier enfermedad que pueda contraer. Por ello, es más que aconsejable dedicar tiempo a revisar la salud de los animales, sin olvidar todas sus vacunas correspondientes. Por lo tanto, es fundamental vacunar a los animales domésticos tanto para conservar su salud como por la nuestra propia.\n\nLA SALUD DE TU AMIGO PUEDE VERSE AFECTADA\n\nEntérate de los síntomas y podrás ayudarle a tiempo\n\nTener un perro es una experiencia maravillosa para todos, salvo que caiga enfermo. Por eso es importante permanecer alerta ante los primeros síntomas que indiquen que su salud puede estar fallando. Para conocer cuáles son las enfermedades que comúnmente afectan a los perros y en qué consisten, Laia Bertan, gerente de AniCura Mima´ns Hospital Veterinary, nos explica todo lo necesario.\n\nIniciando por el moquillo, por ejemplo, que es causado por un virus y afecta a los canes cachorros, se concreta en dificultades al respirar, tics y latiguillos nerviosos, gastroenteritis y dermatitis. En cambio, la hepatitis canina, por lo general produce fiebre, merma del apetito, vómitos, adormecimiento, diarrea, permanente sensación de sed, abundancia de orina, e inflamación del vientre.\n\nLa leptospirosis es una enfermedad zoonótica bacteriana que se adquiere por contacto directo con el agua contaminada por la orina de animales afectados. El peligro es alto porque también se puede contagiar a los humanos. Por otro lado, el parvovirus es una enfermedad viral que tiene consecuencias intestinales serias; en especial, unas diarreas sanguinolentas y fétidas, así como un deterioro progresivo. Debe ser tratado precozmente, o tendrá un pronóstico preocupante.\n\nAdicionalmente, la rabia, que es viral, aguda e infecciosa, ataca el sistema nervioso central y deriva en una encefalitis, letal prácticamente al 100 %. Por su parte, la enfermedad de Lyme, es provocada por garrapatas, que contagian esta afección bacteriana causando daños en la piel, el corazón, los músculos, las articulaciones y el sistema nervioso.\n\nComo ves, la salud de tu mejor amigo puede verse afectada por gran cantidad de causas, incluyendo el sinnúmero que no fueron mencionadas. Tú puedes actuar de manera preventiva y reaccionar con una visita veterinaria ante cualquier primer indicio de alarma. \n\nCONTROL PARASITARIO: UN DESAFÍO NECESARIO\n\nDiferentes especies, mismo fastidio\n\nLos parásitos externos son aquellos que viven en el exterior del cuerpo de nuestra mascota, ya sea sobre la piel o agarrados a los pelos. Para Ubaldo Duarte, en su revista investigativa “Control parasitario en perros y gatos”, entre los más temidos se encuentran las pulgas, que succionan sangre, produciendo muchas ronchas pequeñas. Estas ronchas causan un gran malestar al perro, que no para de rascarse. Como consecuencia, pueden aparecer heridas que favorecen la entrada de patógenos. \n\nPor otro parte, los mosquitos y flebótomos, hacen agujeros en la piel del animal y se alimentan de su sangre. Algunas especies pueden transmitir enfermedades a los perros, algunas de ellas tan graves como la dirofilariosis o gusano del corazón.\n\nTambién existen los ácaros causantes de la sarna; tan diminutos que cavan túneles en la piel de nuestro peludo, alimentándose de ella y ocasionando heridas. Consecuentemente, puede producirse la caída del pelo y aparecer otras enfermedades de la piel, como infecciones de hongos y bacterias.\n\nCuida de tu perro y cuidarás de ti \n\nAunque suelen subestimarse, el control y la prevención de parásitos externos es fundamental para la salud de los peludos y la nuestra, ya que estos constituyen un problema emergente de salud pública al causar enfermedades transmisibles a las personas. \n\nPara combatir estos parásitos, el experto recomienda lavar todos los objetos del perro con el fin de eliminar tanto parásitos como sus formas larvarias, tales como su cama, sus juguetes y los sitios donde suele acostarse. En general, se recomienda limpiar la casa en profundidad, ya que los huevos de las pulgas pueden llegar a los lugares más insospechados. Tampoco se deben descartar las opciones de tratamiento que se adaptan a las distintas necesidades según el paciente y su estilo de vida.",
    "imagen2":"imagenes/salud2.jpg"
    },
    {
    "titulo":"ABANDONO",
    "imagen1":"imagenes/abandono1.jpg",
    "contenido": "CAMOAPA, SUMERGIDA EN UNA SITUACIÓN PREOCUPANTE\n\nLos factores y motivos son diversos\n\n El abandono de caninos es una problemática presente en la comunidad de Camoapa, así como en la gran mayoría de municipios del país. Para Milán Prado, autor de la campaña social “Sensibilización para la protección, cuido y adopción canina”, entre las causas principales de esta situación se encuentra la ignorancia de la población, que no comprende el comportamiento animal; así como la pobreza, puesto que las personas, al no tener suficiente dinero para cuidar a sus animales, terminan echándolos a las calles.\n\n Él expresa, que los propietarios irresponsables también son culpables, ya que muchas veces permiten que los perros se reproduzcan sin control, que deambulen sin supervisión, promocionan la compra de mascotas, y no prestan atención a la salud básica de los caninos. Además, la falta de fondos públicos y que el tema no sea prioridad del gobierno, también constituyen un factor muy importante.\n\nAmbas partes están siendo afectadas\n\nEs evidente que la situación de perros callejeros conlleva resultados negativos tanto para la población, como para los caninos, por ejemplo, la propagación de enfermedades y parásitos, por la cantidad existente de perros enfermos y con lesiones, que en su mayoría son causadas por maltrato. Las mordidas de perros, que son un problema por el trauma físico y mental para las personas afectadas, y por los costos económicos para las familias.\n\nTambién existen las molestias, como ladridos, ruidos, temor, incomodidad (tener que usar calles diferentes), así como contaminación y suciedad, puesto que al romper las bolsas de basura en las calles y haber abundancia de desechos, se generan repercusiones en la salud de otros animales y las personas, pero además una apariencia negativa para la ciudad. Por último, los accidentes de tráfico, aumentan la cantidad de cuerpos muertos, sufrimiento, y pérdidas económicas.\n\nMANERAS EFECTIVAS DE NO MEJORAR LA SITUACIÓN\n\nVeneno, autor de muertes dolorosas\n\nLa población humana ha adoptado distintas maneras para deshacerse de los perros deambulantes. Algunos de estos métodos fáciles, rápidos y baratos de hacerlo son: en primer lugar, la intoxicación de estos pobres animales, considerada erróneamente como una forma de arreglar el problema, ya que muchas veces, resultan tan molestos verlos deambular, que de preferencia se les ofrece alimentos manipulados con sustancias tóxicas para los perros, buscando causarles la muerte; posteriormente, la excusa perfecta es que ayudaron al canino para que no sufra más, pero no se tiene en cuenta que este tipo elementos tóxicos antes de cumplir su objetivo de envenenar al animal, les causa sufrimiento extremo, que debilita sus órganos y sistemas internos hasta que al final mueren.\n\nEl más cruel de todos los métodos\n\nFinalmente, el más cruel, caro y poco efectivo de todos los métodos, debido a que la cifra de perros incluso puede aumentar posteriormente a ser realizada, es el sacrificio de caninos o matanzas clandestinas. De acuerdo con Alberto Nájar, quien escribió un artículo para BBC News respecto al tema, si bien es cierto que los perros callejeros pueden causar problemas en las comunidades, y que pueden ser una amenaza para la salud pública, el sacrificio nunca debería ser considerada una respuesta. La idea de que el sacrificio es la mejor manera de reducir la población de perros o acabar con las amenazas a la salud pública, es totalmente errónea.\n\nTrabajar con las comunidades para examinar las causas de las poblaciones de perros callejeros, como la tenencia irresponsable y la sobre cría, es la mejor manera de encontrar soluciones efectivas que beneficien a ambas partes. En vez de tomar el camino fácil de matar a un perro como parte de una solución más rápida. \n\nPERROS CALLEJEROS: OPINIONES E HISTORIA\n\nLos profesionales camoapenses dicen…\n\nEntre los ciudadanos de nuestro municipio, conocedores del tema de los caninos, encontramos a Alexander Vargas, técnico Veterinario de INTAE, quien expresa que “La principal causa de que existan los perros callejeros es la falta de responsabilidad y compromiso de los dueños. Una campaña de reducción de sobrepoblación de animales sería lo más indicado”. \n\n Por otro lado, Tatiana Reyes, licenciada en Medicina Veterinaria en la UNA - Camoapa, considera que: “El abandono es un acto cruel, pero además constituye una problemática social, porque son transmisores de enfermedades y perjuicios en la comuna. Para tratar de resolverlo, la primera opción sería la adopción, y por su parte, las instituciones, podrían impulsar campañas de castración”.\n\nAlexa, protagonista de una historia inspiradora\n\nEn el barrio San Martín, ubicado en Camoapa, habitaba Alexa, una perrita que al igual que muchos otros, deambulaba día y noche por los alrededores en búsqueda de comida y cariño. Estaba desnutrida, tenía chimones en sus patas y lomo, y un día, quedó embarazada de otro perro callejero, que era mestizo igual que ella.\n\nLuego de dos meses, milagrosamente, dio a luz a sus perritos. Los habitantes del lugar no le prestaron la mínima importancia al suceso, pero una muchacha que visitaba el pueblo la observó a duras penas viva, con los cachorros intentando alimentarse. Ella no lo pensó dos veces y se dijo a sí misma: “No voy a dejar que a estos perritos les pase lo mismo que a ella”, así que buscó ayuda de un veterinario del municipio, que evaluó a Alexa y sus crías, y le dio indicaciones para proseguir con su plan. En la actualidad Alexa ya no sigue con vida, pero sus hijos habitan en Comalapa, con la familia de la joven que un día decidió rescatarla.",
    "imagen2":"imagenes/abandono2.jpg"
    },
    {
    "titulo": "SEGURIDAD",
    "imagen1": "imagenes/seguridad1.jpg",
    "contenido": "BAJO EL RESGUARDO DEL MUNDO Y DEL PAÍS \n\nTurquía y El Salvador: promotores del buen trato a los animales\n\nExisten leyes internacionales que garantizan la protección de todos los animales domésticos y salvajes, entre ellas, las legisladas recientemente en Turquía y El Salvador. Según Roberto Pérez, autor de la investigación “Leyes existentes para la Protección Animal”, Turquía ratificó una nueva ley mundial contra el maltrato animal, que aumenta las sanciones e introduce penas de cárcel para luchar contra los abusos de animales. Esta ley impone penas entre 6 meses y 4 años de cárcel para cualquier persona que de forma deliberada mate una mascota, y más de 3 años de prisión para quienes maten una especie amenazada.\n\nEn el país centroamericano El Salvador, gracias al gobierno de Nayib Bukele se implementó la Ley Especial de Bienestar Animal, que establece la creación del IBA como una institución pública, autoridad superior en materia de aplicación de la política para la protección y bienestar de animales de compañía y animales silvestres.\n\n Ley 747, protectora de nuestras mascotas\n\nEn Nicaragua existe una ley que protege a los animales, la cual fue aprobada por la asamblea nacional el 11 de mayo del 2011 Ley para la Protección y Bienestar de los Animales Domésticos y Animales Silvestres Domesticados. Dicha ley existe, pero no se aplica, ya que la mayoría de la población desconoce o hace caso omiso de esta, incluso las autoridades mismas.\n\nEn referencia a los perros en el ámbito nacional en un artículo del periódico El Nuevo Diario (2012) se dice que, en Nicaragua, los perros son los animales más expuestos a violencia o abandono, esta es la afirmación dada por el doctor Enrique Rimbaud, presidente de la Fundación Amarte, organización al servicio de la defensa y protección de los animales ante situaciones de vulnerabilidad y peligro.\n\nNUESTRA TOMA DE ACCIÓN LOS MANTENDRÁ SEGUROS\n\nConstruyendo una sociedad consciente\n\n Disminuir y erradicar el abandono de perros está en nuestras manos, y para eso, la educación en torno al cuidado y trato de los animales domésticos, en este caso de los perros, se debe iniciar desde una edad temprana, desde casa, para evitar en un futuro que se den casos de abandono. Esta educación sobre los animales se debe reforzar, también, en las escuelas y en las instituciones de enseñanza.\n\nEsterilizar también es amar\n\nLa esterilización es sin duda un procedimiento que contribuye a disminuir el número de perros callejeros. Esta práctica beneficia a que los caninos en este caso, no tengan crías de manera descontrolada, pero, además, favorece a que no corran el riesgo de tener algún padecimiento reproductivo como el cáncer de mama, cáncer de testículos y afecciones uterinas.\n\nAdopción, un acto de humanidad y compromiso\n\nEn la mayoría de los casos, adoptar significa darle una segunda oportunidad a un animal que ha sufrido un proceso de abandono, y en ocasiones maltrato. La veterinaria Brenda Martínez, originaria de Camoapa, expresa que: “Si decides adoptar, debes ser responsable, desparasitarlo, vitaminarlo, darle un buen baño, y, sobre todo, seguir las indicaciones de los profesionales en cuanto a la nueva dieta del mismo”. \n\nTampoco debes esperar que el canino te ame de inmediato, recuerda que muchas veces estos han sido maltratados en las calles y, por tanto, nos temen. Así que deja que vaya a su ritmo, que se acostumbre a tu compañía, y veras como poco a poco, empezará a tomarte afecto.\n\nEn Nicaragua existen organizaciones que rescatan animales, atienden su salud, y les buscan un hogar. A manera de ejemplo, Fundación ADAN es una asociación sin fines de lucro trabaja exhaustivamente para difundir, proteger y promover los derechos de los animales.\n\nDÍA INTERNACIONAL DEL PERRO CALLEJERO \n\n Un recordatorio anual para seguir creando conciencia\n\nEl 27 de julio de cada año, se celebra el Día Internacional del Perro Callejero, una fecha que tiene como propósito generar conciencia sobre la cantidad de perros que se encuentran en situaciones vulnerables buscando alimento en las calles, que han sido abandonados, que han sufrido maltrato por parte de las personas y hasta han sido víctimas de afectaciones por el clima.\n\nEl joven chileno y estudiante de periodismo, Ignacio Gac, fue quien instauró esta fecha para llamar la atención sobre las necesidades que tienen estos animales cuando habitan en la calle. Él expresa que escogió este día del calendario porque julio es el mes más frío y lluvioso de Santiago, capital de su país, y los perros callejeros sufren ante las inclemencias del clima. \n\nComo una salida a esta problemática también propuso la adopción de estas mascotas, para de esta forma no solo reducir la cantidad de perros que deambulan por las vías de las ciudades, sino aumentar la posibilidad de que muchos de ellos tengan hogares dignos y reciban el amor que se merecen.\n\nLa idea de esta fecha es que las personas tomen conciencia de la existencia de los perros callejeros y que puedan ayudarlos de alguna forma. Por ejemplo, se les puede brindar comida, higiene, abrigo y cariño. Lo anterior sin desconocer que se debe tener cuidado y estar alerta a cualquier reacción agresiva del animal.\n\nLa importancia de la celebración de estas fechas es recordar la responsabilidad de protección y respeto que las personas deben tener con los animales y el deber de los gobiernos de desplegar acciones de política pública, como la esterilización, el albergue y la sanción del maltrato, para salvaguardar su integridad física y emocional, con el fin de garantizarles una vida digna.",
    "imagen2":"imagenes/seguridad2.jpg"
    }
    ]
   }
