# Portscanner

Projeto de estudo em C sobre conexões TCP e programação de rede no Windows. O utilitário usa a API Winsock para tentar estabelecer conexões em uma faixa fixa de portas e registrar o resultado no console.

## Compilação

Abra `Portscanner.sln` no Visual Studio 2022 com o workload **Desenvolvimento para desktop com C++**, o toolset MSVC v143 e o Windows SDK. Selecione **Release | x64** e compile a solução.

O ponto de entrada do executável está em `Portscanner/Scandeportas.c`. O arquivo `Portscanner/Arquivo.c` é um exercício separado, mantido como referência.

## Escopo e limitações

- A implementação atual é específica do Windows e faz tentativas TCP sequenciais, com o tempo de espera padrão do sistema.
- Uma falha de conexão pode decorrer de firewall, indisponibilidade ou outras condições de rede. A saída imediata do protótipo não distingue essas causas.
- Use apenas em sistemas próprios ou com autorização explícita.
