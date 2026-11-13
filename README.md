# MTR Diag

**Diagnóstico de rota e perda de pacotes para Windows, com relatório em PDF pronto para o cliente.**

O MTR Diag faz testes de rota (MTR: traceroute + ping contínuo em cada salto), identifica **onde** está a perda de pacotes, a latência ou a instabilidade e gera um relatório claro para enviar ao cliente.

## ⬇️ Download

**[Baixar a versão mais recente](https://github.com/michaelmmichelon/mtr-diag/releases/latest)**: na página do release, baixe o arquivo `MTRDiag-Setup-x.y.z.exe` e execute.

- Windows 10 ou 11 (64 bits). Não precisa instalar nada além do próprio programa.
- Na primeira execução, o Windows pode mostrar *"O Windows protegeu o computador"*, porque o instalador não tem assinatura digital. Clique em **Mais informações → Executar assim mesmo**.
- Depois de instalado, o programa **se atualiza sozinho** quando uma nova versão é publicada aqui.

## O que ele faz

**Teste de rota (MTR)**
- Perda, latência, jitter e qualidade estimada para voz/vídeo (MOS) em cada salto, ao vivo.
- **Operadora de cada salto** (ASN), com o trajeto completo. Exemplo: rede local → provedor → operadora de trânsito → cliente.
- IPv4 e IPv6.

**Diagnóstico automático**
- Diferencia **perda real** (que continua até o destino) de **perda aparente** (roteador que só limita respostas de ping).
- Confirmação ciclo a ciclo: mostra se o salto suspeito perdeu os mesmos pacotes que o destino.
- Aponta o trecho: rede local, Wi-Fi fraco, provedor do cliente, interconexão entre operadoras, IX.
- Destino que bloqueia ping: testa portas TCP e informa se o equipamento está online.
- Teste de MTU (PPPoE, túneis, VPN).

**Relatórios**
- PDF com logo e contato da empresa, gráficos, mapa de perda ao longo do tempo e comparação "antes × depois".
- Resumo em texto para chamado ou WhatsApp, e exportação para Excel (CSV).

**Para o dia a dia do suporte**
- **Vários IPs de uma vez**, com relatório consolidado.
- **Histórico** de todos os testes: reabrir, comparar e gerar o PDF de novo.
- **Monitoramento**: clientes verificados a cada X minutos, com alerta quando há problema, disponibilidade e **relatório mensal** (SLA).
- **App de teste para o cliente**: um programa pequeno (≈75 KB) que você envia ao cliente. Ele testa a conexão a partir da casa/empresa dele, informa se está no Wi-Fi e com qual sinal, e devolve um arquivo `.mtrdiag` que abre direto no MTR Diag.
- Tema escuro e claro.

## Privacidade

- Os testes, o histórico e as configurações ficam **só no seu computador** (`%AppData%\MtrDiag`).
- Para identificar operadoras, o programa consulta os IPs dos saltos nos serviços públicos Team Cymru e RIPEstat. Essa consulta pode ser desligada na tela principal.
- O app do cliente não coleta dados pessoais. Ele só mede a conexão e grava o resultado num arquivo que o próprio cliente decide enviar.

## Versões

As novidades de cada versão estão na página de [Releases](https://github.com/michaelmmichelon/mtr-diag/releases).
