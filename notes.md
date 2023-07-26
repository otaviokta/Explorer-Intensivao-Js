<!-- /*
  Pergunte o nome do usuário e escreva a mensagem:
  "Olá, [nome do usuário]."
*/
let name = prompt("Qual o seu nome?")
alert(`Olá, ${name}. Seja bem vindo.`) -->

---

<!-- /*
  Solicite 2 números, faça a soma deles e apresente o resultado final ao usuário.
*/
alert("Iremos somar dois números.")
let numberOne = prompt("Informe o primeiro número.")
let numberTwo = prompt("Informe o segundo número.")
let soma = Number(numberOne) + Number(numberTwo)
alert(`A soma de ${numberOne} + ${numberTwo} é igual a: ${soma}`) -->

---

<!-- /* Capturar 2 números e fazer as operações matemáticas de soma, subtração, multiplicação, divisão e resto da divisão.
 */

alert("Iremos realizar alguns calculos.")
let numberOne = prompt("Informe o primeiro número: ")
let numberTwo = prompt("Informe o segundo número:")
let soma = Number(numberOne) + Number(numberTwo)
let subtracao = Number(numberOne) - Number(numberTwo)
let multiplicacao = Number(numberOne) * Number(numberTwo)
let divisao = Number(numberOne) / Number(numberTwo)
let restoDivisao = Number(numberOne) % Number(numberTwo)

alert(`A soma dos números ${numberOne} e ${numberTwo} é igual a: ${soma}`)
alert(
  `A subtação dos números ${numberOne} e ${numberTwo} é igual a: ${subtracao}`
)
alert(
  `A multiplicação dos números ${numberOne} e ${numberTwo} é igual a: ${multiplicacao}`
)
alert(`A divisão dos números ${numberOne} e ${numberTwo} é igual a: ${divisao}`)
alert(
  `O resto da divisão do número ${numberOne} por ${numberTwo} é igual a: ${restoDivisao}`
) -->

---

<!-- /\* Solicitar o nome do aluno e as 3 notas do bimestre, em seguida calcular a média daquele aluno. Se o aluno passou no bimestre, dar os parabéns.

Se o aluno não passou no bimestre, motivar o aluno a dar o seu melhor na prova de recuperação.

Em ambos os casos, mostre uma mensagem com o aluno e a média final. \*/

let student = prompt("Qual o nome do(a) aluno(a)?")
let n1 = prompt("Qual a nota da primeira prova?")
let n2 = prompt("Qual a nota da segunda provaw")
let n3 = prompt("Qual a note da terceira prova?")
let average = (Number(n1) + Number(n2) + Number(n3)) / 3
average = average.toFixed(2)

if (average > 6) {
alert(`Parabens ${student}, você passou com a média ${average}`)
} else {
alert(
`Não fique triste ${student}, sua média foi ${average}, estude para a prova de recuperação.`
)
} -->

---

<!-- /_ Capture 10 items para compor a lista de um supermercado. Após caputar os 10 items, imprima-os, separando por vírgula. _/
let items = []
for (let item = 0; item < 10; item++) {
itemName = prompt("Digite o item " + (item + 1))

items[item] = itemName
}

alert(items) -->

---

<!-- /*
Jogo da advinhação

Apresente a mensagem ao usuário:
"Advinhe o número que estou pensando? Está entre 0 e 10"

Cria uma lógica para gerar um número aleatório e verificar se o número digitado é o mesmo que o aleatório gerado pelo sistema.

Enquanto o usuário não adivinhar o número, mostrar a mensagem: "Erro, tente novamente:"

Caso o usuário acerto o número, apresentar a mensagem: "Parabéns! Você advinhou o número em x tentativas"

Substitua o "X" da mensagem, pelo número de tentativas
*/

let result = prompt("Advinhe o número que estou pensando? Está entre 0 e 10")
const randomNumber = Math.round(Math.random() * 10)
const math = Number(result) == randomNumber
let xAttemps = 1

while (Number(result) != randomNumber) {
  result = prompt("Erro, tente novamente:")
  xAttemps++
}

alert(
  `Parabéns! Você adivinhou o número ${randomNumber} em ${xAttemps} tentativas.`
) -->

---

<!-- /*
Faça um programa que tenha um menu e apresente a seguinte mensagem:

Olá usuário! Digite o número da opção desejada

1. Cadastrar um item na lista
2. Mostrar itens cadastrados
3. Sair do programa.

O programa deverá capturar o número digitado pelo usuário e mostrar os seguintes cenários:

Caso o usuário digite 1, ele poderá cadastrar um item em uma lista;
Caso o usuário digite 2, ele poderá ver os itens cadastrados;
  Se não houver nenhum item cadastrado, mostrar e mensagem: "Não existem itens cadastrados."
Caso o usuário digite 3, a aplicação deverá ser encerrada.
*/
let option
let items = []
let index = 0

function teste() {
  option = Number(
    prompt(`Olá Usuário, Digite a opção desejada.\n
1. Cadastrar um item na lista.
2. Mostrar itens cadastrados.
3. Sair do programa.
`)
  )
}

while (option != 3) {
  teste()
  if (option == 1) {
    items[index] = prompt("Informe o nome do item que você deseja cadastrar:")
    index++
  } else if (option == 2) {
    if (items.length == 0) {
      alert("Não existem items cadastrados no sistema.")
    } else {
      alert(items)
    }
  } else {
  }
}

alert("Encerrando o programa.") -->

---

<!-- /* Crie uma lista de pacientes

Cada paciente deverá conter
  - Nome
  - Idade
  - Peso
  - Altura

Escreva uma lista contendo o nome dos pacientes */

const pacientes = [
  {
    name: "Luiz",
    age: 20,
    weight: 100,
    height: 190,
  },
  {
    name: "Alexandra",
    age: 27,
    weight: 70,
    height: 170,
  },
  {
    name: "Carlos",
    age: 42,
    weight: 90,
    height: 180,
  },
]

let pacientesName = []

for (let paciente of pacientes) {
  pacientesName.push(
    `${paciente.name} tem ${paciente.age} anos, pesa ${paciente.weight} kg e tem ${paciente.height} de altura.\n`
  )
}

alert(pacientesName) -->

---

<!-- /\*
Dada uma lista de pacientes, descubra o IMC de cada paciente e imprima

"Paciente X possui o IMC de: Y"

Onde X é o nome do paciente e Y é o IMC desse paciente

Crie uma função para fazer o cálculo de IMC
\*/

/_ peso / (altura _ altura) \*/

const patients = [
{
name: "Luiz",
age: 20,
weight: 100,
height: 190,
},
{
name: "Alexandra",
age: 27,
weight: 70,
height: 170,
},
{
name: "Carlos",
age: 42,
weight: 90,
height: 180,
},
]

function IMC(weight, height) {
return (weight / (height / 100) \*\* 2).toFixed(2)
}

function printPatientIMC(patient) {
return `    Paciente ${patient.name} possui o IMC de
    ${IMC(patient.weight, patient.height)}
 `
}

for (let patient of patients) {
let IMCmessage = printPatientIMC(patient)
alert(IMCmessage)
} -->
