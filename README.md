# AJAX
### Resumo do Código: Busca de Endereço por CEP

Este código HTML implementa um formulário que permite ao usuário inserir um CEP e automaticamente preencher os campos de endereço com base na informação obtida através da API ViaCEP.

#### Funcionalidades:

1. **Estrutura do Formulário**:
   - O formulário contém campos para o CEP, rua, bairro, cidade e estado.
   - O método de envio do formulário está configurado para `POST` para a rota `/submit-endereco`.

2. **Validação do CEP**:
   - Quando o campo do CEP perde o foco (evento `onblur`), a função `buscarEndereco()` é chamada.
   - A função verifica se o CEP possui 8 dígitos, exibindo um alerta se o CEP for inválido.

3. **Requisição à API ViaCEP**:
   - Utiliza a API ViaCEP para buscar informações de endereço correspondentes ao CEP inserido.
   - Em caso de sucesso, os campos de rua, bairro, cidade e estado são preenchidos automaticamente com os dados retornados.

4. **Tratamento de Erros**:
   - A função possui um bloco `try...catch` para lidar com possíveis erros durante a requisição da API, exibindo um alerta caso ocorra uma falha.
