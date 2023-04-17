# importar selenium e criar navegador para a automação web 

from selenium import webdriver
from webdriver_manager.chrome import ChromeDriverManager
from selenium.webdriver.chrome.service import Service

servico = Service (ChromeDriverManager().install())

navegador = webdriver.Chrome(service=servico)

# entrar no site ( meu caso um site do minicuros da hashtagprogramação)

navegador.get("https://pages.hashtagtreinamentos.com/inscricao-minicurso-python-automacao-org?origemurl=hashtag_yt_org_minipython_videoselenium")

# se inscrever , inserindo nome e email
navegador.find_element('xpath', 
                       '//*[@id="section-10356508"]/section/div[2]/div/div[2]/form/div[1]/div/div[1]/div/input').send_keys("AlysonLima")
navegador.find_element('xpath', 
                       '//*[@id="section-10356508"]/section/div[2]/div/div[2]/form/div[1]/div/div[2]/div/input').send_keys("alysonlimateste@gmail.com")
# clicar em enviar 
navegador.find_element('xpath', '//*[@id="section-10356508"]/section/div[2]/div/div[2]/form/button').click()
