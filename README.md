# tugas-4

let studentsScore = [
  { name: 'Andi', score: 90 },
  { name: 'Rudi', score: 80 },
  { name: 'Dira', score: 100 }
];

// Cari siswa dengan nilai tertinggi
let highest = studentsScore[0];

for (let i = 1; i < studentsScore.length; i++) {
  if (studentsScore[i].score > highest.score) {
    highest = studentsScore[i];
  }
}

// Tampilkan hasil
console.log("Siswa dengan nilai tertinggi adalah:");
console.log("Nama:", highest.name);
console.log("Nilai:", highest.score);

var motoGP = [
  {
    circuit: "Losail",
    location: "Doha",
    winner: {
      firstname: "Andrea",
      lastname: "Dovizioso",
      country: "Italy"
    }
  },
  {
    circuit: "Autodromo",
    location: "Argentina",
    winner: {
      firstname: "Cal",
      lastname: "Crutchlow",
      country: "UK"
    }
  },
  {
    circuit: "De Jerez",
    location: "Spain",
    winner: {
      firstname: "Valentino",
      lastname: "Rossi",
      country: "Italy"
    }
  },
  {
    circuit: "Mugello",
    location: "Italy",
    winner: {
      firstname: "Andrea",
      lastname: "Dovizioso",
      country: "Italy"
    }
  }
];

// Kelompokkan data berdasarkan negara pemenang
var groupedByCountry = {};

for (let i = 0; i < motoGP.length; i++) {
  let winnerCountry = motoGP[i].winner.country;
  let circuitName = motoGP[i].circuit;

  // Jika negara belum ada di objek, buat array baru
  if (!groupedByCountry[winnerCountry]) {
    groupedByCountry[winnerCountry] = [];
  }

  // Tambahkan nama sirkuit ke negara tersebut
  groupedByCountry[winnerCountry].push(circuitName);
}

// Tampilkan hasil
console.log(groupedByCountry);
