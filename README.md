# Classificação de Imagens em Tempo Real com Keras e OpenCV

Um projeto simples para classificar imagens em tempo real usando um modelo pré-treinado do Teachable Machine (Keras) e a webcam do computador.

---

## 📌 Descrição
Este projeto utiliza um modelo de **classificação de imagens** exportado do Teachable Machine para detetar e classificar objetos em tempo real através da webcam. O script captura frames, processa-os no formato necessário e exibe a classe prevista junto com o *score* de confiança diretamente na imagem.

---

## ⚠️ Aviso Importante: Compatibilidade
Para garantir que o modelo `.h5` funcione corretamente (evitando erros de `groups: 1` nas camadas de convolução causados pelo Keras mais recente), é **obrigatório** utilizar o **TensorFlow 2.15.0**. Versões superiores podem apresentar incompatibilidades com modelos exportados do Teachable Machine.

---

## 🛠 Requisitos
- Python 3.10 ou superior
- Webcam funcional

---

## 📥 Instalação e Configuração

### 1. Clonar o repositório:
```bash
git clone https://github.com/rs_silva1977/keras_opencv.git
cd keras_opencv
```

### 2. Criar e Ativar um Ambiente Virtual (Recomendado):
É fundamental usar um ambiente virtual para evitar conflitos de versões no seu sistema.

**No Windows:**
```bash
python -m venv venv_ia
.\venv_ia\Scripts\activate
```

**No Linux/macOS:**
```bash
python3 -m venv venv_ia
source venv_ia/bin/activate
```

### 3. Instalar as dependências:

**Opção A (Recomendada - Automática):**
Utilize o arquivo `requirements.txt` para instalar todas as versões compatíveis de uma só vez:
```bash
pip install -r requirements.txt
```

**Opção B (Manual - Para conferência):**
Caso prefira instalar manualmente, utilize exatamente estas versões testadas:
```bash
pip install tensorflow==2.15.0 numpy==1.26.4 opencv-python
```

### 4. Preparar os ficheiros necessários:
Certifique-se de que os seguintes arquivos estão na pasta raiz do projeto:
- `keras_model.h5` (O modelo exportado do Teachable Machine)
- `labels.txt` (Arquivo de texto com os nomes das classes, uma por linha)

---

## 🚀 Como Usar

1. **Com o ambiente virtual ATIVADO**, execute:
```bash
python classificador_imagens.py
```

2. **Interagir com o programa:**
- Uma janela com a imagem da webcam será aberta.
- O nome da classe detetada e o *score* de confiança serão exibidos na tela.
- Pressione **ESC** ou feche a janela para encerrar o programa.

---

## 📂 Estrutura do Projeto
```
.
├── keras_model.h5          # Modelo pré-treinado (Keras/TF)
├── labels.txt              # Nomes das classes (uma por linha)
├── classificador_imagens.py # Script principal de processamento
├── requirements.txt        # Lista de dependências e versões fixas
└── README.md               # Documentação do projeto

---

## 🔧 Personalização

- **Modelo:** Substituir `keras_model.h5` pelo teu modelo pré-treinado.
- **Classes:** Atualizar `labels.txt` com as classes correspondentes ao teu modelo.
- **Resolução:** Ajustar o tamanho da imagem no script (`224x224` por padrão) se o teu modelo exigir outra resolução.

---

## 📝 Notas

- O modelo deve estar treinado para **224x224 pixels** e **3 canais de cor (RGB)**.
- O ficheiro `labels.txt` deve conter **uma classe por linha**, na mesma ordem das saídas do modelo.
- Para melhor performance, certifica-te que a webcam está a funcionar corretamente.

---

## 🤝 Contribuições

Contribuições são bem-vindas! Sente-te à vontade para abrir *issues* ou *pull requests*.

---

## 📜 Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).
