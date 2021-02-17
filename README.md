# OAuthTwitch

Code source du script issu de la vidéo : https://www.youtube.com/watch?v=ersavK0Zl9o 

# Documentation
<hr>

## Installer et configurer
### Installer
- Créer une application et la configurer https://dev.twitch.tv/

- Cloner le dépôt `git clone https://github.com/NoS1gnalWeb/OAuthTwitch`

- Configurer `src > config.php` avec l'identifiant, le secret, le lien de redirection et les scopes.
<hr>

### Configurer

1) Créer le lien pour se connecter <br>
```php
$link = $oauth->get_link_connect();
```
Twitch va retourer un code avec le protocle `GET` il suffira donc de tester la variable.

2) Obtenir le token
```php
$token = $oauth->get_token($code);
```

3) Configurer les headers pour les requêtes vers l'API 
```php
$oauth->set_headers($token);
```

4) Exemple : recherche d'une chaîne
```php
$query = $oauth->search_channel($channel);
```

<hr>

# Exemple de code 
bientôt


# Licence
Open source
