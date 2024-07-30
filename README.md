PokeApiDemo
Descrição
API em C# para interagir com a PokéAPI, permitindo obter informações de Pokémon, registrar mestres Pokémon e capturas de Pokémon.

Tecnologias Usadas
Linguagem: C#
Framework: ASP.NET Core
Banco de Dados: SQLite
ORM: Entity Framework Core
Outras Dependências:
Newtonsoft.Json
Como Instalar e Usar
Pré-requisitos
.NET SDK 6.0+
SQLite
Passos para Instalar
Clone o repositório:
bash
Copiar código
git clone https://github.com/USERNAME/PokeApiDemo.git
cd PokeApiDemo
Configure a conexão com o banco de dados no arquivo appsettings.json, caso necessário.

Restaure as dependências e crie o banco de dados:

bash
Copiar código
dotnet restore
dotnet ef migrations add InitialCreate
dotnet ef database update
Execute o projeto:
bash
Copiar código
dotnet run
Endpoints Disponíveis
GET /api/pokemon/random: Obter 10 Pokémon aleatórios.
GET /api/pokemon/{id}: Obter um Pokémon específico por ID.
POST /api/master: Cadastrar um mestre Pokémon (dados básicos como nome, idade e CPF).
POST /api/pokemon/capture: Informar que um Pokémon foi capturado.
GET /api/pokemon/captured: Listar os Pokémon já capturados.
Exemplo de Uso
Cadastrar um Mestre Pokémon:

bash
Copiar código
curl -X POST "https://localhost:5001/api/master" -H "accept: text/plain" -H "Content-Type: application/json" -d "{\"name\":\"Ash Ketchum\",\"age\":10,\"cpf\":\"123.456.789-00\"}"
Obter 10 Pokémon Aleatórios:

bash
Copiar código
curl -X GET "https://localhost:5001/api/pokemon/random" -H "accept: text/plain"
Informar a Captura de um Pokémon:

bash
Copiar código
curl -X POST "https://localhost:5001/api/pokemon/capture" -H "accept: text/plain" -H "Content-Type: application/json" -d "{\"id\":1,\"name\":\"Pikachu\",\"masterName\":\"Ash Ketchum\"}"
.gitignore
Certifique-se de adicionar um .gitignore para evitar arquivos desnecessários no repositório. Aqui está um exemplo básico para um projeto .NET:

plaintext
Copiar código
## Ignore Visual Studio temporary files, build results, and
## files generated by popular Visual Studio add-ons.

# User-specific files
*.rsuser
*.suo
*.user
*.userosscache
*.sln.docstates

# User-specific files (Mono Auto Generated)
mono_crash.*

# User preferences for mono
mono_crash.*

# Build results
[Dd]ebug/
[Dd]ebugPublic/
[Rr]elease/
[Rr]eleases/
x64/
x86/
[Aa][Rr][Mm]/
[Aa][Rr][Mm]64/
bld/
[Bb]in/
[Oo]bj/
[Ll]og/
[Ll]ogs/
[Tt]mp/
[Oo]ut/
[Pp]ublish/
.lock.json

# VS Code directories
.vscode/
.history/
Challenge
This is a challenge by Coodesh.
