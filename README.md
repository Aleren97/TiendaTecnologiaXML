# README TRABAJO GRUPAL 1 DEL 2DO TRIMESTRE


## CONTEXTO ELEGIDO
    El contexto que se ha elegido para este trabajo es el del Inventario de una empresa Tecnológica.


## ESTRUCTURA DEL XML
    * La estructura del XML esta hecha por la declaración de que el archivo es XML.
    
    * Seguido del DOCTYPE para enlazarlo con el archivo estructura.dtd.
    
    * A continuación tenemos la etiqueta raíz del documento llamada "tecnologia".
    
    * Despúes dentro de esta tenemos los elementos "item" los cuales tienen el atributo de "id" el cual es obligatorio.
    
    * Dentro de cada "item" encontramos las etiquetas "nombre", "marca", "precio" y "stock".


## LO QUE VALIDA EL DTD
    En el archivo de estructura.dtd tenemos distintas etiquetas con "!ELEMENT" para el dtd como:
    
    * El elemento "tecnologia" el cual es el elemento raíz el cual tiene "(item+)" lo cual indica que "tecnologia" tiene varias etiquetas "item".
    
    * El elemento "item" tiene dentro de unos parentesis los elementos que van a ir dentro sí o sí, seguido del mismo elemento "item" pero esta vez dandole el atributo "id" junto a #REQUIRED, lo cual significa que el atributo "id" es obligatorio.
    
    * Por último uno debajo del otro tenemos los elementos que estan dentro del elemento "item" que son "nombre", "marca", "precio" y "stock".


## LO QUE VALIDA EL XSD
    En el archivo de esquema.xsd tenemos diferentes etiquetas con "xs:" para el xsd como:

    * Primero se empieza con la declaración xml en el archivo xsd.

    * Abrimos con la eitqueta "xs:schema" que es el elemento raíz del xsd.

    * Después tenemos el elemento de nombre "tecnologia" en el cual tenemos dentro dos etiquetas más: 
        - "xs:complexType" -> que indica que este elemento contiene otros en su interior.
        - "xs:sequence" -> que indican que los siguientes elementos deben aparecer en el orden definido.

    * Dentro tenemos al elemento "item" en el cual tenemos (maxOccurs="unbounded") que lo que nos indica es que se pueden tener más de un item y dentro tenemos otros "complexType" y "sequence".

    * Por ultimo tenemos los distintos elementos dentro del item que son "nombre", "marca", "precio" y "stock" los cuales tienen al lado (type="") para indicar el tipo de dato que es cada elemento.
        - nombre -> string
        - marca -> string
        - precio -> integer
        - stock -> integer
    El string es una variable de tipo texto y el integer es otra variable de tipo número.


## DIFICULTADES ENCONTRADAS DURANTE EL DESARROLLO
    Las dificultades que se tuvieron dentro del trabajo fueron el implementar el cómo saber que los distintos archivos estaban validados lo cual se solucionó mediante una busqueda en internet de la extensión que permitía ver esta validación.