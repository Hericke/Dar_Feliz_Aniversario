# Dar_Feliz_Aniversario

Para postar no Facebook, podemos utilizar a API Graph do Facebook. Primeiro, precisamos criar um aplicativo no Facebook Developer e obter um token de acesso válido para fazer as chamadas da API. Em seguida, podemos usar a biblioteca facebook-sdk para Python e o método put_object() para publicar uma mensagem de feliz aniversário na timeline do usuário:


import facebook

# define as credenciais do aplicativo
APP_ID = 'seu_app_id'
APP_SECRET = 'seu_app_secret'
ACCESS_TOKEN = 'seu_access_token'

# inicializa o objeto GraphAPI com as credenciais
graph = facebook.GraphAPI(access_token=ACCESS_TOKEN, version='3.0')

# escreve a mensagem de feliz aniversário
mensagem = "Feliz Aniversário! 🎉🎂🎁"

# publica a mensagem na timeline do usuário
graph.put_object(parent_object='me', connection_name='feed', message=mensagem)

Twitter
No Twitter, podemos utilizar a API REST do Twitter para postar uma mensagem de feliz aniversário. Novamente, é necessário obter as credenciais de acesso à API do Twitter antes de poder fazer as chamadas da API. Podemos usar a biblioteca tweepy para Python e o método update_status() para postar a mensagem na timeline do usuário:

import tweepy

# define as credenciais de acesso à API do Twitter
CONSUMER_KEY = 'seu_consumer_key'
CONSUMER_SECRET = 'seu_consumer_secret'
ACCESS_TOKEN = 'seu_access_token'
ACCESS_SECRET = 'seu_access_secret'

# autentica com a API do Twitter
auth = tweepy.OAuthHandler(CONSUMER_KEY, CONSUMER_SECRET)
auth.set_access_token(ACCESS_TOKEN, ACCESS_SECRET)
api = tweepy.API(auth)

# escreve a mensagem de feliz aniversário
mensagem = "Feliz Aniversário! 🎉🎂🎁"

# publica a mensagem na timeline do usuário
api.update_status(mensagem)


Instagram
No Instagram, a API não permite mais postagens diretas na timeline do usuário. Em vez disso, podemos usar o módulo instabot para Python para enviar uma mensagem de feliz aniversário como mensagem direta para a pessoa:

from instabot import Bot

# inicializa o objeto bot
bot = Bot()

# faz login no Instagram
bot.login(username='seu_username', password='sua_senha')

# escreve a mensagem de feliz aniversário
mensagem = "Feliz Aniversário! 🎉🎂🎁"

# envia a mensagem direta para a pessoa
bot.send_message(mensagem, ['usuário_do_aniversariante'])


Observe que este método requer que você siga a pessoa no Instagram e que ela também esteja seguindo você para poder enviar uma mensagem direta.

Esses são apenas alguns exemplos simples de como integrar com as APIs de algumas redes sociais para postar uma mensagem de feliz aniversário. É importante lembrar que cada rede social tem sua própria documentação de API e requisitos de autenticação, então é necessário pesquisar e verificar as especificidades para cada caso.












