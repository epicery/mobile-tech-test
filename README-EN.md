# Mobile Epicery Exercise: Candidate Citizens

### Functional needs

> Our presidential candidate needs a tool to get to know his potential future voters a little better.

The software editor asks you to develop an Android, iOS or Flutter mobile application with two IHM. The first one will display all the citizens, the second one the contact information of a particular citizen. The software editor has not yet met a designer and therefore leaves you free for IHM design.

### Ressources

The list of French citizens is accessible at the address `https://randomuser.me/api/1.4/` with `GET` method.
For this first MVP, only 100 randomly chosen French citizens will be used. This list is accessible adding the parameters `?nat=FR&results=100`.

### Exemple

The webservice will return a list of citizens in `JSON` :

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

In this example :

- the citizen name is Léo Blanchard
- he is 49 years old
- his photos are available in value of the "picture" key, choose the most relevant for each screen
- his mail is leo.blanchard@example.com
- his phone number is 06-00-59-53-98

### Features

1. The first screen must display all citizens (name +  age + picture).
2. The first screen must display contact informations of one of them (name + picture + age + mail + phone number).
3. To improve his targeting, he would like to be able :
  - filter citizens by department (keys `location>state`)
  - that the list of citizens be ordered by age starting with the youngest
4. The software editor is also open to any proposal that seems relevant to his needs.


The quality of the code prevailing over the quantity of features, only the first two are mandatory.


### Roadmap/Technical informations

> You can fill here all the ideas for improving the code, technical choices if necessary or any information necessary to build your proposal.

*The software editor wishes you good luck and looks forward to discovering your proposal.*