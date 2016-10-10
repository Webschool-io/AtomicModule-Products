# AtomicModule-Products

  Módulo atômico para gerenciar os atributos de produtos de um e-commerce.
## Conceito

  Esse modulo deverá conter dos os atributos para cadastro de produto, e será ultilizado para cadastrar produtos e manter a manutenção com futuras edições.

## Funcionalidades

  - Fazer o CRUD no objeto Produtos

## Interface


### Cadastrar novo produto;

      - name: addProduct
      - params: {product}
        - product: objeto do tipo produto
      - retorno: Object
        {
            status: String
          , message: String
          , code: Number
          , idTransaction: Number
        }

### Atualizar produto;

      - name: setProduct
      - params: {product},
        - product: objeto do tipo produto
      - retorno: Object
        {
            status: String
          , message: String
          , code: Number
          , idTransaction: Number
        }

### Busca produto
  - nome: findProduct
  - params: product.idProduct
    - product.idProduct: atributo de identificação do produto.
  - retorno: Object
    {
        status: String
      , message: String
      , code: Number
      , idTransaction: Number
      , object: []
    }

### Remover produto
  - nome: removeProduct
  - params: product.idProduct
    - product.idProduct: atributo de identificação do produto.
  - retorno: Object
    {
        status: String
      , message: String
      , code: Number
      , idTransaction: Number
      , object: []
    }


## Tipos

### productType

  - type: object
  - schema:

    {
        idProduct: number
       , datePublish: date
       , name: String
       , status: boolean
       , visible: boolean
       , type: String
       , enableStock: bollean
       , shortDescription: String
       , description: String
       , tag: {tag: String}
       , category: {category: String}
       , prices: {priceName: String, value: number, valuePromo: number}
       , ref: number
       , weight: number
       , length: number
       , width: number
       , height: number
       , attribute: {attributeName: String, Value: String}
       , note: String
       , featuredImage: String
       , galeryImage: {order: number, image: String}
    }




## Todo retorno de função será um objeto
###Objeto de retorno
    {
        status: String
      , message: String
      , code: Number
      , idTransaction: Number
    }

  - status: Status com mensagens padronizadas tipo: "success", "error" (ainda não definidas)
  - message: Mensagem de retorno
  - code:  códigos padrões à serem ainda definidos
  - idTransaction: id da tentativa
