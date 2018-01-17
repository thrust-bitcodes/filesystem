Filesystem
===============

Filesystem é um *bitcode* de manipulação de arquivos para [ThrustJS](https://github.com/thrustjs/thrust).

# Instalação

Posicionado em um app [ThrustJS](https://github.com/thrustjs/thrust), no seu terminal:

```bash
thrust install filesystem
```

## Tutorial

```javascript
let fs = require('filesystem')

let meuJson = fs.readJson('meuJson.json')
show(meuJson)
```

O modulo filesystem contém os seguintes métodos

```javascript
/**
   * @desc Apaga o arquivo *filePathName*.
   * @param {string} filePathName - caminho absoluto ou relativo do arquivo a ser apagado.
   * @returns {boolean} - retorna *true* se a operação foi executada sem erro e *false* caso contrário.
   */
  delete(filePathName)

  /**
   * @desc Verifica se o arquivo *filePathName* existe.
   * @param {string} filePathName - caminho absoluto ou relativo do arquivo que se deseja verificar a existência.
   * @returns {boolean} - *true* if the file exists; *false* if the file does not exist or its existence cannot be determined.
   */
  exists(filePathName)

  /**
   * @desc Lê o conteúdo do arquivo *filePathName* e retorna em uma string.
   * @param {string} filePathName - caminho absoluto ou relativo do arquivo a ser lido e ter o seu conteúdo retornado.
   * @param {java.nio.charset.Charset} charset - o *charset* as ser usado para decodificação (default é UTF_8)
   * @returns {string} - o conteúdo do arquivo.
   * @throws Irá gerar uma exceção caso ocorra algum problema ao ler o arquivo.
   */
  readAll(filePathName, charSet)

  /**
   * @desc Lê o conteúdo do arquivo *filePathName* em formato JSON e retorna o objeto.
   * @param {string} filePathName - caminho absoluto ou relativo do arquivo a ser lido e ter o seu conteúdo retornado.
   * @param {java.nio.charset.Charset} charset - o *charset* as ser usado para decodificação (default é UTF_8)
   * @returns {string} - o conteúdo do arquivo.
   * @throws Irá gerar uma exceção caso ocorra algum problema ao ler o arquivo.
   */
  readJson(filePathName, charSet)

  /**
   * @desc Read all lines from a file as a Stream. Unlike readAllLines, this method does not read
   *       all lines into a List, but instead populates lazily as the stream is consumed.
   * @param {string} fileObject - caminho absoluto ou relativo do arquivo a ser lido e ter o seu conteúdo retornado.
   * @param {java.nio.charset.Charset} charset - o *charset* as ser usado para decodificação (default é UTF_8)
   * @returns {java.util.stream.Stream<String>} - the lines from the file as a Stream.
   */
  lines(fileObject, charSet)

  /**
   * @desc Salva a string passada no parâmetro *content* para o arquivo definido por *filePathName*.
   * @param {string} filePathName - caminho absoluto ou relativo do arquivo o qual receberá o conteúdo.
   * @param {string} content - o conteúdo a ser gravado no arquivo.
   */
  saveToFile(fileName, content)
```
