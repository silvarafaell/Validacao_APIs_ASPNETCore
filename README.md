Curso Validação de APIs com ASP.NET Core no nextwave(LuisDEV)

### Validação de APIs
 - Uma das maiores dores de cabeça de um programador é tratar dados inconsistentes no banco de dados
 - É confiar que dados como a seguir vão vir corretos:
   - CEP
   - Nome da Cidade
   - CPF
   - Email
   - Telefone
 - Prevenir é muito mais barato do que gastar muito tempo apagando incêncido por falta de validação na API
 - A estrutura ideal de validação em um sistema
   - Validação no cliente (front-end, como app, web, ou desktop)
   - Validação na entrada da API
   - Validação a nível de domínio

 ### O que é Fluent Validation
  - Biblioteca utilizada para validação de objetos, portanto permitindo ser utilizada para verificar nossos modelos de entrada (Commands / Input Models)
  - Instalada na aplicação através do pacote FluentValidation.AspnetCore
  - São criadas classes de validação para cada modelo de entrada a ser validado
  - Como utilizar esta biblioteca, o fluxo é:
    - Configurar o Fluent Validation de forma global
    - Criar uma classe que herde de AbstractValidator<T>
    - Implementar as regras no construtor através do método RuleFor
  - Caso prefira fazer de formal manual, é possivel utilizar injeção de dependência para obter o objeto IValidator<T>, onde terá acesso ao método Validate e seu resultado, checando a propriedade IsValid
  - Funcionalidades do Fluent Validation
    - Validações de propriedades simples
    - Validações de propriedades complexas
    - Validação de listas
    - Multiplos validadores para a mesma classe
  - Métodos de validação mais utilizados
    - NotNull, NotEmpty
    - Equal, NotEqual
    - Length, MaxLength, MinLength
    - LessThan, LessThanOrEqualTo, GreaterThan, GreaterThanOrEqualTo
    - Must
    - EmailAddress
    - CreditCard
    - IsInEnum
    
