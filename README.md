# rastgelekelime

[![NPM](https://img.shields.io/badge/NPM-red?logo=NPM&style=flat-square)](https://www.npmjs.com/package/rastgelekelime)

## Bir yada daha fazla Türkçe kelime çıktısı alın.

Kurulum:

    npm install rastgelekelime

Kullanım:

    var kelime = require('rastgelekelime');

    console.log(kelime()); // Bir adet çıktı almanızı sağlar.

    console.log(kelime(5)); // Belirlediğiniz kadar (Örn:5) çıktı almanızı sağlar.

    console.log(kelime({ min: 3, max: 10 })); // Belirli sayı aralığı kadar (örn: 3-10 arası) çıktı almanızı sağlar.

    console.log(kelime({ exactly: 2 })); // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar.

    console.log(kelime({ exactly: 5, join: ' ' })) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. Çıktı alınan kelimelerin arasına belirlediğiniz karakteri (örn: boşluk) koyar.

    console.log(kelime({ exactly: 5, join: '' })) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. Çıktı alınan kelimelerin arasına bir şey koymaz, yapışık çıktı verir.

    console.log(kelime({exactly: 5, maxLength: 4})) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. En fazla belirlediğiniz uzunlukta (örn: 4) çıktı almanızı sağlar.

    console.log(kelime({exactly:5, wordsPerString:2})) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar.

    console.log(kelime({exactly:5, wordsPerString:2, separator:'-'})) // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar. Çıktı alınan kelimelerin arasına belirlediğiniz karakteri (örn: -) koyar.

    console.log(kelime({exactly:5, wordsPerString:2, formatter: (word)=> word.toUpperCase()})) // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar. Çıktıların tüm harflerini büyük harfle yazdırır.

    console.log(kelime({exactly:5, wordsPerString:2, formatter: (word, index)=> {return index === 0 ? word.slice(0,1).toUpperCase().concat(word.slice(1)) : word;}}))  // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar. Çıktıların ilk harfini büyük yazdırır.

Random-words [NPM](https://www.npmjs.com/package/random-words) - [GitHub](https://github.com/punkave/random-words) üzerinde değişiklikler yapılarak oluşturulmuştur.
