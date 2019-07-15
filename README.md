# ayuda-djs
Necesitas ayuda?, Esta es tu pagina!

Con esta pagina vas a poder conseguir más de 5 ejemplos para ayudarte:

1

2

3

4

5

6

7

8

9

10
Errores que te pueden pasar:

Unexpected token (

Unexpected token )

Unexpected token

Ejemplos-djs:

```Por favor les recomiendo no solo copiar y pegar, y si no has manipulado ninguna base de datos o esta base de datos anteriormente les recomiendo que aprendan acerca de su función al menos antes de tener contacto con este código. Bueno, atentos a las notas. Este es un ejemplo del comando marry/casamiento
const db = require("megadb")
const db_marry = new db.crearDB("marry")
const Discord = require("discord.js") // <- Para los que no usen handler no coloquen esto de acá

module.exports.run = (client, message, args) => { // para los que no usen handler, este exports de acá no lo coloquen

// if (command === "marry"){  //Para los que no usan handler

const usuario = message.mentions.users.first() || client.users.get(args[0]);

if (!usuario) return message.channel.send("Este usuario no existe. Método: `!marry <@usuario/usuarioid>`");

message.channel.send(`${usuario.tag}, aceptas la propuesta de ${message.author.tag}?`)

const collector = message.channel.createMessageCollector(m => m.author.id === usuario.id && m.channel.id === msg.channel.id, {time : 30000}); // Creamos una colección de mensajes acá
collector.on("collect", message => { // llamados al evento de la coleción
    if (message.content.toLowerCase() === "yes"){  // Condicionamos una respuesta al decir yes
        message.channel.send("Felicidades a la nueva pareja")
        db_marry.establecer(message.author.id, usuario.id) // Guardamos en cada pareja la id de su esposx
        db_marry.establecer(usuario.id, message.author.id)
message.stop()
    } else if (message.content.toLowerCase() === "no"){ // Acá otra respuesta al decir que no
        message.channel.send("Parece que la propuesta ha sido rechazada")
message.stop()
    }
});

collector.on("end", collected => { // Esto es por si se acaba el tiempo
    if (collected.size === 0) return message.channel.send("Parece que alguien huye del matrimonio :rolling_eyes:");
});
}```
