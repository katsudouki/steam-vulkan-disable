# Proton Desabilitador de Vulkan - Steam (Linux)

Este script foi desenvolvido para desabilitar o Vulkan nas versões do Proton instaladas na Steam para Linux. <br>
Ele força o Proton a usar o WineD3D em vez do Vulkan para rodar jogos<br>
o que pode ser útil em placa de video antigas e casos onde o Vulkan causa problemas de desempenho ou compatibilidade.

## ⚙️ Como Funciona

1. **Identificação dos diretórios Steam**: O script busca automaticamente os diretórios onde a Steam está instalada no seu sistema, especificamente o diretório `common/` que contém os jogos e os módulos Proton.
   
2. **Busca por versões do Proton**: Ele identifica todas as versões do Proton instaladas, procurando por diretórios que comecem com o prefixo `Proton`.

3. **Configuração do WineD3D**: Para cada versão do Proton encontrada, o script cria ou sobrescreve o arquivo `user_settings.py` com a configuração necessária para forçar o uso do WineD3D:
   ```python
   user_settings = {
       "PROTON_USE_WINED3D": "1",
   }
   ```
<br>
📋 Requisitos
Steam: Certifique-se de ter a Steam instalada e com Proton habilitado nas configurações na aba compatibilidade.
Linux: Este script foi projetado para sistemas operacionais baseados em Linux.
<br><br>
🚀 Como Usar

primeiro baixe com o curl
```bash
curl -LO https://raw.githubusercontent.com/katsudouki/steam-vulkan-disable/refs/heads/master/vulkandisabler
```
adicione as permissao de executar:
```bash
chmod +x vulkandisabler
```
e finalmente rode o script com :
```bash
./vulkandisabler
```

O script irá perguntar se você deseja continuar, descrevendo o que ele fará. Basta responder com s para confirmar.


⚠️ Atenção
Este script deve ser usado após instalar uma versão do Proton na Steam.

💬 Contribuições
Se você encontrar algum bug ou tiver sugestões de melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.

📝 Licença
Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para mais detalhes.

🖥️ Cores ANSI Utilizadas<br>
Verde: Utilizado para mensagens de sucesso e informações gerais.<br>
Amarelo: Utilizado para destacar textos importantes ou variáveis.<br>
Ciano: Usado para cabeçalhos e divisão de seções.<br>
Vermelho: Utilizado para alertas ou mensagens de erro.<br>
