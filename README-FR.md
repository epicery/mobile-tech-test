# Exercice Mobile Epicery: Les citoyens du candidat

### Expression de besoin fonctionnel

> Notre candidat à la présidentielle a besoin d'un outil lui permettant de connaître un peu mieux ses potentiels futurs électeurs.

L’éditeur vous demande de développer une application mobile Android, iOS ou Flutter comprenant deux interfaces. L'une doit permettre de voir l'ensemble des citoyens, la deuxième les informations de contact d'un citoyen en particulier. L'éditeur n'a pas encore rencontré de designer et vous laisse donc carte blanche pour l'interface


### Ressources

La liste des citoyens français est accessible à l’adresse `https://randomuser.me/api/1.4/` en `GET`.
Pour ce premier MVP, seuls 100 citoyens français choisis au hasard seront récupérés. Cette liste est accessible ajoutant les paramètres `?nat=FR&results=100`.

### Exemple

Le service renverra une liste de citoyens en `JSON` :

```json
{
    "results": [
        {
            "gender": "male",
            "name": {
                "title": "Mr",
                "first": "Léo",
                "last": "Blanchard"
            },
            "location": {
                "street": {
                    "number": 3745,
                    "name": "Rue de Gerland"
                },
                "city": "Amiens",
                "state": "Tarn",
                "country": "France",
                "postcode": 62264,
                "coordinates": {
                    "latitude": "-83.9885",
                    "longitude": "-6.4817"
                },
                "timezone": {
                    "offset": "+4:30",
                    "description": "Kabul"
                }
            },
            "email": "leo.blanchard@example.com",
            "login": {
                "uuid": "91a580e9-7044-4f7d-8f87-782a2732e067",
                "username": "lazyladybug526",
                "password": "zelda",
                "salt": "Ddqs9CYH",
                "md5": "129b926f4289a8b38404dc4cf5329085",
                "sha1": "bd81407944cdb580ef27985fb526c80c3c3217d2",
                "sha256": "98abb761eaf78d4f101548ff97697b48ea7753039829c42b9ba17c5cd7727c5b"
            },
            "dob": {
                "date": "1973-01-12T19:45:55.620Z",
                "age": 49
            },
            "registered": {
                "date": "2005-06-10T12:33:26.155Z",
                "age": 17
            },
            "phone": "01-41-19-04-42",
            "cell": "06-00-59-53-98",
            "id": {
                "name": "INSEE",
                "value": "1730000206759 07"
            },
            "picture": {
                "large": "https://randomuser.me/api/portraits/men/65.jpg",
                "medium": "https://randomuser.me/api/portraits/med/men/65.jpg",
                "thumbnail": "https://randomuser.me/api/portraits/thumb/men/65.jpg"
            },
            "nat": "FR"
        }
    ],
    "info": {
        "seed": "a1f9baa06069eae7",
        "results": 1,
        "page": 1,
        "version": "1.4"
    }
}
```

Dans cet exemple :

- le nom du citoyen est Léo Blanchard
- il a 49 ans
- ses photos sont disponibles en valeur de la clef "picture", choisir la plus pertinente pour chaque écran
- son email est leo.blanchard@example.com
- son téléphone portable est 06-00-59-53-98

### Features

1. Le premier écran doit d’afficher tous les citoyens (nom +  âge + photo) récupérés du webservice.
2. Le second doit montrer les informations de contact d'un citoyen (nom + photo + âge + mail + numéro de téléphone).
3. Afin d'affiner ses ciblages, il aimerait pouvoir :
  - filtrer les citoyens par département (clefs `location>state`)
  - que la liste soit par ordre d'âge en commençant par les plus jeunes
4. L'éditeur est également ouvert à toute proposition qui vous semblerait pertinente pour ses besoins

La qualité du code prévalant sur la quantité des features, seules les deux premières sont obligatoires.


### Roadmap/Informations techniques

> Vous pouvez renseigner ici toutes les pistes d'amélioration du code, choix techniques si besoin ou toute information nécessaire pour faire builder votre proposition.

*L'éditeur vous souhaite bon courage et a hâte de découvrir votre proposition.*
