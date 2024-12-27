 * WHAT IS MY EMAIL PROVIDER?
 * ==========================
 
 * Email merupakan sebuah cara untuk kita berinteraksi antar satu dengan yang lainnya secara elektronik,
 * Banyak sekali provider yang menyediakan layanan email ini.
 
 * Buatlah sebuah proses yang akan mengeluarkan output provider email yang digunakan oleh user.
 
 * Contoh:
 *    Input  : jhon@development.com
 *    Output : Your email provider is enigmacamp
      (tidak menggunakan .com di belakang)
      
 * RULES:
 *    Tidak diperbolehkan menggunakan built-in function:
 *     .map .filter .reduce .split .join .indexOf .findIndex .substring

 * JAWABAN:
``` function emailProvider(input) { // fungsi emailProvider
    let output = "" // Penampung Kata yang di cari
    let flag = false // Penanda Looping
    for (let char of input) { // Tolong looping char dari input
        if (char === "@") { // jika char bernilai @
            flag = true // maka ubah flag menjadi true
            continue // lanjutkan looping
        }
        if (char === ".") { // jika char bernilai .(titik)
            break // maka hentikan looping
        }
        if (flag) { // Jika char bernilai true
            output += char // Maka tambahkan output dengan char
        }
    }
    // return output // kembalikan output
}
console.log(emailProvider('jhon@development.com')) // output: 'development')


function emailProvider(input) { // fungsi emailProvider
    let output = "" // Penampung Kata yang di cari
    let flag = false // Penanda Looping
    for (let char of input) { // Tolong looping char dari input
        if (char === "@") { // jika char bernilai @
            flag = true // maka ubah flag menjadi true
            continue // lanjutkan looping
        }
        if (char === ".") { // jika char bernilai .(titik)
            break // maka hentikan looping
        }
        if (flag) { // Jika char bernilai true
            output += char // Maka tambahkan output dengan char
        }
    }
    return output // kembalikan output
}
console.log(emailProvider('jhon@xyz.com')) // output: 'xyz'
```
