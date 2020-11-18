# ProjetosEmPython
8 Projetos em Python 
from PySimpleGUI import PySimpleGUI as sg

sg.theme('Reddit')

layout=[
        [sg.Text('Tela de Cadastro')],
        [sg.Text('Email:'),sg.Input(key='usuario')],
        [sg.Text('Senha:'),sg.Input(key = 'senha',password_char= '*')],
        [sg.Checkbox('Salvar o Login?')]
        [sg.Button('ENTRAR')]
]
janela = sg.Window('Tela do seu Cadastro', layout)

while True:
    eventos, valores = janela.Read()
    if eventos == sg.WINDOW_CLOSED:
        break
    if eventos == 'ENTRAR':
        if valores['usuario'] == 'vinicius' and valores['senha'] == '12345678':
            print('Cadastro concluído bem-vindo')
        else:
            print('Dados informados incorretos')
