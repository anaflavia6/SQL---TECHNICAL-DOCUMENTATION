# SQL---TECHNICAL-DOCUMENTATION
Esse documento tem como finalidade observar como o estudo do **Basic SQL** se finaliza, e se está apto para os próximos passos, visando aprimorar habilidades e construir uma base técnica estável.

## Technical Base (Base Técnica)

Não se pode pintar um carro antes dele estar montado, o processo no **Database (BD)** é o mesmo, logo vejamos sua estrutura hierárquica (**Query Execution Order**).

1. **FROM (The Beginning):** O início. O banco de dados localiza a tabela (**Data Source**). Sem definir a origem, não há matéria-prima para o processo.
    
2. **WHERE (Decision Flow):** Fluxograma Sim ou não? O Carro já foi montado? Se sim, segue para a pintura; se não, continua procurando. É o filtro que impede que dados irrelevantes sobrecarreguem o sistema.
    
3. **SELECT (The Choice):** Só após juntar todas as partes que você poderá chamar aquele conjunto de metais de "carro" e então escolher a cor da pintura (**Projection**). Aqui definimos quais colunas serão exibidas.
    
4. **ORDER BY (Final Polish):** Faz a organização estética para garantir uma boa apresentação final (**Sorting**). É o polimento que coloca os resultados na sequência correta (alfabética ou numérica).
   
    <img width="1024" height="768" alt="diagrama anaflavia" src="https://github.com/user-attachments/assets/3e402d85-a027-4350-bfa0-43038dbda130" />


A ideia de filtrar os dados no **WHERE** antes de escolher o que vai aparecer no **SELECT** é porque garante uma testagem se a pesquisa está sendo bem executada (**Performance and Validation**). Ter os comandos de "sim ou não" ajuda a sinalizar erros e otimizar o tempo de resposta do banco de dados antes de prosseguir para as etapas finais.


<img width="1363" height="597" alt="image" src="https://github.com/user-attachments/assets/e64faba2-029e-48e5-bce1-0cfbc06b8146" />

---

## Applied Patterns (Padrões Aplicados)

Para validar essa base técnica, foram aplicados conceitos fundamentais em desafios reais:

### 1. Multiple Constraints (Filtros Compostos)

Uso do operador `AND` para garantir que o "carro" atenda a mais de um requisito de qualidade antes de sair da linha de produção.

- **Exemplo:** Filtrar funcionários com `salary > 2000` **AND** `months < 10`.
    

### 2. String Manipulation & Pattern Matching

- **Index -3:** É pedir para o SQL ler de trás para frente (**Right-to-left reading**). Útil para encontrar padrões no final das palavras, como extensões ou sufixos específicos.
    
- **REGEXP:** Implementação de expressões regulares para buscas complexas (ex: nomes que começam e terminam com vogais), funcionando como um scanner de alta precisão na linha de montagem.
    

### 3. Error Prevention (Prevenção de Erros)

- **Function Syntax:** A ausência de espaços entre o nome da função e os parênteses (ex: `SUBSTR()`) evita falhas de interpretação do **SGBD**.
    
- **Literal Typing:** Diferenciação entre números (sem aspas) e textos (com aspas) para manter a integridade dos dados.
