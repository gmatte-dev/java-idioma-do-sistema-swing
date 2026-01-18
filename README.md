# Detector de Idioma do Sistema

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Swing-GUI-blue?style=for-the-badge" alt="Swing">
  <img src="https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=for-the-badge" alt="Status">
</p>

## Sobre o Projeto

Aplicacao desktop desenvolvida em **Java** com interface grafica **Swing JFrame** que identifica e exibe o idioma configurado no sistema operacional do usuario, utilizando a classe `Locale` do Java.

---

## Origem do Projeto

> Este projeto foi desenvolvido durante o **Curso de Java - 40 Horas** ministrado pelo professor **Gustavo Guanabara** no [Curso em Video](https://www.cursoemvideo.com/).

O curso oferece uma base solida em programacao Java, abordando desde conceitos fundamentais ate a criacao de interfaces graficas com Swing.

---

## Conceitos Utilizados

### Classe Locale

A classe `java.util.Locale` representa uma regiao geografica, politica ou cultural especifica. Ela e usada para adaptar informacoes ao usuario, como:

- Idioma do sistema
- Pais/Regiao
- Formatacao de datas e numeros
- Moeda local

### Principais Metodos

| Metodo | Descricao |
|--------|-----------|
| `Locale.getDefault()` | Retorna o Locale padrao do sistema |
| `getLanguage()` | Retorna o codigo do idioma (ex: "pt") |
| `getCountry()` | Retorna o codigo do pais (ex: "BR") |
| `getDisplayLanguage()` | Retorna o nome do idioma por extenso |
| `getDisplayCountry()` | Retorna o nome do pais por extenso |

---

## Como Funciona

```
1. A aplicacao e iniciada
2. O programa captura as configuracoes de Locale do sistema operacional
3. Extrai informacoes como:
   - Codigo do idioma
   - Nome do idioma
   - Codigo do pais
   - Nome do pais
4. Exibe todas as informacoes na interface grafica
```

---

## Funcionalidades

- [x] Deteccao automatica do idioma do sistema
- [x] Exibicao do codigo do idioma (ISO 639)
- [x] Exibicao do nome do idioma por extenso
- [x] Exibicao do codigo do pais (ISO 3166)
- [x] Exibicao do nome do pais por extenso
- [x] Interface grafica intuitiva com Swing JFrame
- [x] Botao para atualizar informacoes

---

## Screenshot

```
+-----------------------------------------------+
|         DETECTOR DE IDIOMA DO SISTEMA         |
+-----------------------------------------------+
|                                               |
|   Informacoes do Sistema                      |
|   -------------------------                   |
|                                               |
|   Codigo do Idioma:    pt                     |
|                                               |
|   Nome do Idioma:      Portugues              |
|                                               |
|   Codigo do Pais:      BR                     |
|                                               |
|   Nome do Pais:        Brasil                 |
|                                               |
|   Locale Completo:     pt_BR                  |
|                                               |
+-----------------------------------------------+
|            [ ATUALIZAR ]                      |
+-----------------------------------------------+
```

---

## Pre-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

- **Java JDK 8** ou superior
- Uma IDE de sua preferencia (NetBeans, Eclipse, IntelliJ IDEA, VS Code)

---

## Como Executar

1. **Clone o repositorio**
   ```bash
   git clone https://github.com/seu-usuario/detector-idioma-java.git
   ```

2. **Acesse a pasta do projeto**
   ```bash
   cd detector-idioma-java
   ```

3. **Compile o projeto**
   ```bash
   javac Main.java
   ```

4. **Execute a aplicacao**
   ```bash
   java Main
   ```

> **Dica:** Se estiver usando uma IDE como NetBeans ou Eclipse, basta abrir o projeto e clicar em "Run".

---

## Estrutura do Projeto

```
detector-idioma-java/
|
+-- src/
|   +-- Main.java               # Classe principal
|   +-- TelaIdioma.java         # Interface Swing
|
+-- README.md
```

---

## Tecnologias Utilizadas

- **Java SE** - Linguagem de programacao
- **Swing** - Biblioteca para interface grafica
- **JFrame** - Container principal da aplicacao
- **JLabel** - Exibicao das informacoes
- **JButton** - Botao de acao
- **Locale** - Classe para obtencao do idioma do sistema

---

## Logica Principal

```java
import java.util.Locale;

public class DetectorIdioma {
    
    public static void main(String[] args) {
        // Obtem o Locale padrao do sistema
        Locale locale = Locale.getDefault();
        
        // Codigo do idioma (ex: pt, en, es)
        String codigoIdioma = locale.getLanguage();
        
        // Nome do idioma por extenso
        String nomeIdioma = locale.getDisplayLanguage();
        
        // Codigo do pais (ex: BR, US, ES)
        String codigoPais = locale.getCountry();
        
        // Nome do pais por extenso
        String nomePais = locale.getDisplayCountry();
        
        // Locale completo (ex: pt_BR)
        String localeCompleto = locale.toString();
        
        // Exibindo no console
        System.out.println("Codigo do Idioma: " + codigoIdioma);
        System.out.println("Nome do Idioma: " + nomeIdioma);
        System.out.println("Codigo do Pais: " + codigoPais);
        System.out.println("Nome do Pais: " + nomePais);
        System.out.println("Locale Completo: " + localeCompleto);
    }
}
```

---

## Exemplos de Resultado

| Sistema | Codigo Idioma | Nome Idioma | Codigo Pais | Nome Pais |
|---------|---------------|-------------|-------------|-----------|
| Brasil | pt | Portugues | BR | Brasil |
| Portugal | pt | Portugues | PT | Portugal |
| Estados Unidos | en | English | US | United States |
| Espanha | es | Espanol | ES | Espana |
| Franca | fr | Francais | FR | France |
| Alemanha | de | Deutsch | DE | Deutschland |
| Japao | ja | Japanese | JP | Japan |

---

## Aprendizados

Durante o desenvolvimento deste projeto, foram aplicados os seguintes conceitos:

- Programacao Orientada a Objetos (POO)
- Criacao de interfaces graficas com Swing
- Utilizacao da classe Locale
- Internacionalizacao (i18n) em Java
- Obtencao de informacoes do sistema operacional
- Manipulacao de strings
- Manipulacao de eventos (ActionListener)

---

## Possiveis Melhorias

- [ ] Exibir a bandeira do pais detectado
- [ ] Mostrar o fuso horario do sistema
- [ ] Exibir formato de data e hora local
- [ ] Mostrar o formato de moeda do pais
- [ ] Permitir alterar o idioma da interface
- [ ] Listar todos os idiomas disponiveis no sistema

---

## Contribuicoes

Contribuicoes sao sempre bem-vindas! Se voce tem alguma sugestao para melhorar este projeto:

1. Faca um Fork do projeto
2. Crie uma Branch para sua feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudancas (`git commit -m 'Adiciona NovaFeature'`)
4. Push para a Branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

---


## Autor

Desenvolvido durante o **Curso de Java 40 Horas** do [Curso em Video](https://www.cursoemvideo.com/)

**Professor:** Gustavo Guanabara

---

## Links Uteis

- [Curso em Video - Java](https://www.cursoemvideo.com/curso/java-basico/)
- [Documentacao Java](https://docs.oracle.com/en/java/)
- [Tutorial Swing](https://docs.oracle.com/javase/tutorial/uiswing/)
- [Classe Locale - Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)
- [ISO 639 - Codigos de Idiomas](https://pt.wikipedia.org/wiki/ISO_639)
- [ISO 3166 - Codigos de Paises](https://pt.wikipedia.org/wiki/ISO_3166-1)

---

<p align="center">
  Se este projeto te ajudou, considere dar uma estrela!
</p>
