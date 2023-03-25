1. Cambiar el nombre de la columna "lng" por "lon" para que Tableau pueda plotearlo en un mapa
```
df = df.rename(columns={'oldName1': 'newName1', 'oldName2': 'newName2'})

df = df.rename(columns={'lng':'lon'})
```

2. Las columnas que su dtype esta como object, determinar si es requerido modificar de object a category

3. La columna City, almacena el nombre de la ciudad y del pais separado por "," ```Querétaro ,Mexico```

4. La columna *sentiment_dictionary* almacena el valor 'AFINN' y no se que significado tiene

5. La columna *sentiment_value* almacena los siguiente valores:  3, -3,  2,  1, -1,  4, -5, -2,  5, -4,  0. ¿A que se refieren estos valores? Significara que el valor mas alto es el más querido? 

6. La columna *verified* almacena 0 y 1, supongo que 0 significa, no verificado y 1 significa SI verificado

7. La columna *account_created_at*, es la fecha de la creación de la cuenta de Twitter. Se debe convertir a formato fecha

8. La columna *created_at* es la fecha de la creación del tweet. Se debe convertir a formato fecha

9. Las columnas favourites_count, statuses_count, friends_count,  followers_count, retweet_count, favorite_count no se a que se refieren. Ya viendo las columnas con mas detalle, son columnas de cuentas. Por ejemplo, favourites_count, es la cuenta de favoritos de . . . 

10. La columna *description* es el tweet
11. La columna *name* es el nick de la cuenta
12. La columna *lang* se refiere al lenguaje usado en el tweet
13. La columna *is_retweet* supongo que evalua si es o  no un retweet. 0 es NO y 1 es SI
14. La columna *reply_to_user_id* es el id del usuario al que replicaron un tweet. 
15. La columna *reply_to_status_id*  . .  supoooongo que se refiere a la replica que le hicieron al estatus de un usuario.
16. La columna *source*, es la mas interesante, porque alamacena el origen del tweet 🧐 e identifica si el origen fue a partir de un dispositivo android o IOS o si es un bot
17. La columna *text* es realmente la del tweet. Entonces a que se refiere description?
18. No ubico a que se refiere la columna *screen_name*
19. La columna *status_id* almacena numerooootes.
20. El user_id es el id del usario

## Jerga de Twitter

RT o re-tweet (retuit) es un tweet de otra persona que comparti en mi cuenta y que se puede ver a traves de ella. Se ve en mi feed.

cuando hago un re-tweet de un tweet, mis seguidores lo veran y queda guardado en mi perfil junto a las tweets que he escrito.

Cuando a un tweet le marco me gusta y lo marco como favorito y se queda almacenado en mi apartado de favoritos. Cuando alguien entre a mi perfil, podra verlo en el apartado y no en el feed general.

Direct Message DT o mensaje directo, es le medio por el cual se envia un mensaje privado a un usuario

Timeline o TL de Twitter o conocido como cronologia en español y se observa en la pestaña principal del Twitter y se van observando los tweets que van entrando de los usuarios que sigo

Fandom, es un grupo de gente que comparte interes por un tema determinado

follow es cuando se sigue a un suario

unfollow es cuando dejar de seguir un usuario y dejo de ver sus publicaciones

Como usar los hashtag

Un tweet permite 280 caracteres. cuando un mensaje requiere mas palabras para transmitir el mensaje, entonces de crea un *hilo*. Un hilo es un conjunto de tweets relacionados entre si.

Para crear un hilo, primero se escribe un tweet. Al terminar el primer tweet, se hace click en el gisno de + para ir agregando tweets referentes al primero y asi se crean los hilos.

Citar tweet: 