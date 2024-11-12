# Token Argon2 Pour Vaultwarden

## Argon 2 ?

*Argon2 est un algorithme de dérivation de clé conçu pour le hachage sécurisé des mots de passe.*

## Comment créer ce token ? 

Pour créer le jeton on à besoin de taper cette commande : 

```sh
docker run --rm -it vaultwarden/server /vaultwarden hash
```

On spéficie ensuite le mot de passe souhaité, on obtiens alors un token sous ce format : 

```sh
ADMIN_TOKEN=$argon2id$v=19$m=65540,t=3,p=4$CeciEstUnExempleDeTokenArgon2$abcdef+GhIJK1Mn0qr5TUvWxyZ
```
