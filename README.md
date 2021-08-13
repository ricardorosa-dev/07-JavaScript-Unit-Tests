<h1 align="center">Testes Unitários em JavaScript</h1>

![GitHub repo size](https://img.shields.io/github/repo-size/ricardorosa-dev/05-project-meme-generator?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/ricardorosa-dev/05-Project-Meme-Generator?style=for-the-badge)

<p>
<img src="imgs/preview.gif" />
</p>

> Projeto para o aprendizado de manipulaçao da DOM, Eventos e Web Storage

> HTML5 | CSS3 | JavaScript

### ✨ [Demo](https://ricardorosa-dev.github.io/projects/05-meme-generator)

## Author

👤 **Ricardo Rosa**

* Website: http://ricardorosa-dev.github.io/
* Github: [@ricardorosa-dev](https://github.com/ricardorosa-dev)
* LinkedIn: [@https://ricardorosa-dev.github.io/projects/03-toto-list/index.html](https://ricardorosa-dev.github.io/projects/03-toto-list/index.html)

---
## Funções

### Average
```JavaScript
const average = (array) => {
  let m = 0;
  if (array.length < 1) {
    return undefined;
  }
  for (let i = 0; i < array.length; i += 1) {
    if (typeof array[i] !== 'number') {
      return undefined;
    }
    m += array[i];
  }
  return Math.round(m / array.length);
};
```
### Testes
```JavaScript
describe('#average', () => {
  it("tests function average's behaviour as specified", () => {
    assert.strictEqual(average([3, 4, 5]), 4);
    assert.strictEqual(average([1, 2, 3, '4', 5]), undefined);
    assert.strictEqual(average([0, 0, 0, 0, 0, 0, 0]), 0);
    assert.strictEqual(average([1, 2, '3']), undefined);
    assert.strictEqual(average([1, 2, 3]), 2);
    assert.strictEqual(average([0, 0, 0, 0, 0, 0, 1]), 0);

    assert.strictEqual(average([]), undefined);
    assert.strictEqual(average([' ']), undefined);
    assert.strictEqual(average(['um', 'dois', 'tres']), undefined);
    assert.strictEqual(average([47, 63, 122]), 77);

    assert.strictEqual(average([-11, 2, 5]), -1);

    assert.strictEqual(average([-11, -5, 2]), -5);
  });
});
```

### Create Student
```JavaScript
const createStudent = (nome) => {
  const estudante = {
    name: nome,
    feedback: () => 'Estudante criado',
  };
  return estudante;
};
```
### Testes
```JavaScript
describe('#createStudent', () => {
  it('returns the object as specified', () => {
    const estudante = createStudent('Leandrão, o Lobo Solitário');
    assert.strictEqual(typeof estudante, 'object');
    assert.strictEqual(typeof estudante.feedback, 'function');
    assert.strictEqual(estudante.name, 'Leandrão, o Lobo Solitário');
    assert.strictEqual(estudante.feedback(), 'Eita pessoa boa!');

    const estudante2 = createStudent('Nobre');
    assert.strictEqual(typeof estudante2, 'object');
    assert.strictEqual(typeof estudante2.feedback, 'function');
    assert.strictEqual(estudante2.name, 'Nobre');
    assert.strictEqual(estudante2.feedback(), 'Eita pessoa boa!');

    const estudante3 = createStudent('Inácio');
    assert.strictEqual(typeof estudante3, 'object');
    assert.strictEqual(typeof estudante3.feedback, 'function');
    assert.strictEqual(estudante3.name, 'Inácio');
    assert.strictEqual(estudante3.feedback(), 'Eita pessoa boa!');
  });
});
```
---



## Show your support

Give a ⭐️ if this project helped you!

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
