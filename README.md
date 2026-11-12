# SimCity 3000 — Edição Web Clássica

Uma experiência de construção e administração de cidades diretamente no navegador, com interface inspirada na apresentação clássica de *SimCity 3000*.

> **Status:** protótipo web jogável. O projeto é executado no navegador e não exige instalação de dependências ou servidor próprio.

## Jogar

Depois de ativar o GitHub Pages, abra o endereço publicado pelo GitHub. Para testar localmente, basta abrir `index.html` em um navegador moderno.

## Recursos presentes no projeto

- Mapa isométrico em grade 128 × 128 e diferentes terrenos iniciais.
- Opção de iniciar uma cidade vazia ou carregar a cidade-modelo “Vila Maxis”.
- Ferramentas de consulta, movimentação, demolição, terreno, zoneamento, transporte, serviços públicos e estruturas cívicas.
- Controles de velocidade, rotação e zoom do mapa.
- Camadas de visualização para mapa, subsolo, energia, água, poluição, criminalidade, valor do terreno e serviços.
- Painéis de orçamento, população, demanda RCI, conselheiros, ordenanças, acordos com cidades vizinhas e gráficos históricos.
- Eventos e desastres, incluindo incêndios, tornados, terremotos, OVNIs e colapsos nucleares.
- Salvamento no armazenamento local do navegador e importação/exportação de cidades em JSON.
- Interface adaptada para mouse e toque, com atalhos de teclado.

## Controles de teclado

| Tecla | Ação |
|---|---|
| `W` `A` `S` `D` ou setas | Mover a câmera |
| `Q` / `E` | Girar o mapa |
| `+` / `-` | Aproximar / afastar |
| `Espaço` | Pausar / retomar a simulação |
| `1` / `2` / `3` | Velocidade da simulação |
| `H` | Selecionar ferramenta de movimentação |
| `B` | Selecionar demolição |
| `F` | Selecionar consulta |
| `Esc` | Fechar janelas e consulta |

Os controles visuais na interface também podem ser usados sem teclado.

## Publicar com GitHub Pages

1. Crie um repositório no GitHub, por exemplo `simcity3000-web`.
2. Envie os arquivos deste diretório para a raiz do repositório. O arquivo principal precisa permanecer com o nome `index.html`.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)`, depois salve.
6. Aguarde a publicação e acesse o endereço indicado na própria página de configurações do Pages.

Não é necessário configurar Node.js, Actions, bundlers ou dependências externas para a versão atual.

## Estrutura

```text
simcity3000-web/
├── index.html   # jogo completo (HTML, CSS, JavaScript e sprites embutidos)
└── README.md    # apresentação, controles e instruções de publicação
```

## Observações

- O progresso salvo no navegador fica no armazenamento local daquele navegador/dispositivo. Para transportar uma cidade, use a opção de exportar JSON.
- O projeto não possui backend nem sincronização online de cidades.
- Este é um projeto independente, não oficial e sem afiliação com a Electronic Arts ou com os criadores de *SimCity*. “SimCity” e marcas relacionadas pertencem aos respectivos titulares. Esta página não afirma possuir direitos sobre marcas ou materiais de terceiros eventualmente presentes.
- Nenhuma licença de código foi incluída. Antes de adicionar uma licença aberta ou redistribuir/publicar sprites e outros materiais de terceiros, confirme que você possui os direitos necessários.

## Desenvolvimento

A implementação atual está concentrada em `index.html`. Para modificar a interface, os estilos estão no bloco `<style>`; a lógica do jogo está no bloco `<script>`.
