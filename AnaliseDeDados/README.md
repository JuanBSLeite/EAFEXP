# Intro do módulo Instrumentação em física de partículas II

Explorar o universo subatômico é um desafio que tem impulsionado a física desde os tempos do atomismo grego. À medida que a ciência avançou, a compreensão da matéria em escalas cada vez menores exigiu o desenvolvimento de tecnologias de detecção sofisticadas e colaborações internacionais extensas. Essas parcerias globais têm sido essenciais para lidar com os altos níveis de energia necessários para criar e observar novas partículas, além de permitir a coleta massiva de dados indispensáveis para a detecção de eventos raros Neste curso, focamos na teoria e prática dos detectores de partículas, instrumentos vitais que permitiram grandes avanços na física moderna. Abordaremos desde os princípios fundamentais da interação da radiação com a matéria até as mais recentes inovações tecnológicas em detectores. Além de explorar a história e o desenvolvimento desses dispositivos, discutiremos suas aplicações práticas, que vão desde a pesquisa básica em aceleradores de partículas até o estudo dos raios cósmicos. Os alunos participarão de demonstrações práticas de técnicas de detecção e aquisição de dados. O curso incluirá medidas de coincidência, medidas de energia de partículas com detector Cherenkov de água, e trajetografia de múons cósmicos, utilizando detectores a gás da tecnologia RPC (Resistive Plate Chamber) e cintiladores plásticos com fotomultiplicadoras de silício (SiPM). Durante o curso, os alunos construirão um detector de raios cósmicos e receberão uma introdução à HDL (Hardware Description Language), com o objetivo de desenvolver um pequeno sistema embarcado em FPGA para medir fluxo/trajetória de múons e a energia depositada por raios cósmicos. Além disso, realizarão simulações e análises de dados utilizando as ferramentas Geant4 e Root.

Info adicional aqui: https://eafexp.cbpf.br/modulos/2

# Repositório

Neste repositório vocês encontrarão tudo que é necessário para esse módulo: 

- Firmware das FPGAs
- Notebooks
- Dados coletados para as primeiras aulas

Para utilizar esse notebook é recomendado que tenham os seguintes softwares instalados:

- Python 3
    - recomendamos instalar usando o miniconda : https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions
- Visual Studio Code
    -   Windows: https://go.microsoft.com/fwlink/?LinkID=534107
    - Linux: https://code.visualstudio.com/docs/setup/linux
- Quartz 13.1 lite
    - Windows: https://www.altera.com/downloads/fpga-development-tools/quartus-ii-web-edition-design-software-version-13-1-windows
    - Linux - https://www.altera.com/downloads/fpga-development-tools/quartus-ii-web-edition-design-software-version-13-1-linux

# Preparando o ambiente

Para rodar os notebooks, precisamos criar o ambiente python com as bibliotecas que vamos utilizar durante a análise de dados.


No terminal, siga os passos a seguir;

```bash
# onde preferir crie uma pasta chamada HEPII
mkdir HEPII

# mude para a pasta
cd HEPII

# clone o repositório do modulo 
git clone git@git.cbpf.br:eafexp/2026.git

cd EAFEXP

# mude para o Branch do módulo
git checkout HEPII

cd ..

# crie o ambiente python .hepenv fora da pasta EAFEXP
python -m venv .hepenv
# ou python3

# ative o ambiente
source .hepenv/bin/activate

# instale as dependências
pip3 install -r EAFEXP/AnaliseDeDados/requirements.txt

# abra o visual code na pasta HEPPII
code .

# isso irá abrir uma janela do VScode.
```

# Alternativa 2 - Jupyterhub

Outra alternativa é utilizar o ambiente de computação em nuvem do INCT-CERN, o Jupyterhub. 

- https://jupyterhub.inct-cern.cbpf.br/hub/login?next=%2Fhub%2F

Para logar, basta utilizar seu e-mail institucional.

Para salva permanentemente seus arquivos, abra um terminal e acesse o caminho `/shared_data/EAFEXP26/`e crie uma pasta com seu nome `mkdir arrascaeta`. 

Essa será sua pasta de trabalho. Para acessa-la pelo painel do jupyter, crie um atalho `ln -s /shared_data/EAFEXP26/arrascaeta ~/arrascaeta`. A sua pasta irá aparecer na barra lateral do jupyter.

Atenção, ao realizar as atividades do módulo, abra sempre o kernel com cvmfs no nome.






