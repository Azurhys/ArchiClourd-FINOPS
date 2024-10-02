## Cognitive Service

![Alt text](./aiservice.png?raw=true "Vnet")


## API Text Analytics

```py
import requests

# Informations de connexion à l'API
subscription_key = "accec0862d234731b54a32b679bf46e3"
endpoint = "https://cognitivelab8.cognitiveservices.azure.com/"
path = "/text/analytics/v3.0/sentiment"

def get_sentiment(text):
    headers = {"Ocp-Apim-Subscription-Key": subscription_key}
    documents = {"documents": [{"id": "1", "text": text}]}
    response = requests.post(endpoint + path, headers=headers, json=documents)
    return response.json()

# Exemple d'analyse de sentiment
text = "Azure Cognitive Services are amazing!"
result = get_sentiment(text)
print(result)
```

## Metrics

![Alt text](./metrics.png?raw=true "Vnet")