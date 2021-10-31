## Solución lab2 - IW
+ Rubén Subías Rodríguez (759406)

The instructions used to build and run the server and the client are the following:

+ **Server:**

```
./gradlew :server:build     // Build

./gradlew :server:run       // Run
```

+ **Client:**

```
./gradlew :client:build     // Build

./gradlew :client:run       // Run
```

For making the server work correctly, it was also needed to complete the translation code in the server side:

```
fun translation(@RequestPayload request: TranslationRequest): TranslationResponse = 
        TranslationResponse().apply{ 
            translation = "hola"
    }
```
After changing the text input in *client.kt* to the desired input and building and running both the server and the client, we obtain the following output:

```
Result of translating [hello] is [hola]
```