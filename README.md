<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Routing Statis dan Dinamis</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: linear-gradient(to right, #1e3c72, #2a5298);
            color: white;
        }
        header {
            text-align: center;
            padding: 20px;
            background: rgba(0,0,0,0.4);
            animation: fadeIn 2s;
        }
        h1 {
            margin: 0;
        }
        .container {
            padding: 20px;
        }
        .card {
            background: rgba(255,255,255,0.1);
            padding: 15px;
            margin: 15px 0;
            border-radius: 10px;
            animation: slideUp 1s;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
            background: white;
            color: black;
        }
        table, th, td {
            border: 1px solid black;
        }
        th {
            background: #2a5298;
            color: white;
        }
        th, td {
            padding: 10px;
            text-align: left;
        }
        ul {
            margin-left: 20px;
        }

        /* Animasi */
        @keyframes fadeIn {
            from {opacity: 0;}
            to {opacity: 1;}
        }

        @keyframes slideUp {
            from {transform: translateY(50px); opacity: 0;}
            to {transform: translateY(0); opacity: 1;}
        }
    </style>
</head>
<body>

<header>
    <h1>Routing Statis dan Dinamis</h1>
</header>

<div class="container">

    <div class="card">
        <p>
            Routing adalah proses pengiriman paket data melalui jaringan dari satu perangkat ke perangkat lainnya.
            Terdapat dua metode utama yaitu <b>Static Routing (Statis)</b> dan <b>Dynamic Routing (Dinamis)</b>.
        </p>
    </div>

    <div class="card">
        <h2>1. Static Routing (Routing Statis)</h2>
        <p>
            Static Routing adalah jenis routing di mana administrator jaringan secara manual memasukkan
            informasi rute ke dalam tabel routing router.
        </p>

        <h3>Karakteristik:</h3>
        <ul>
            <li>Manual: Admin harus tahu semua alamat network tujuan</li>
            <li>Tetap: Jalur tidak berubah jika link gagal</li>
            <li>Resource rendah: Tidak membebani CPU dan bandwidth</li>
        </ul>

        <h3>Kelebihan & Kekurangan:</h3>
        <table>
            <tr>
                <th>Kelebihan</th>
                <th>Kekurangan</th>
            </tr>
            <tr>
                <td>Beban CPU ringan</td>
                <td>Tidak cocok untuk jaringan besar</td>
            </tr>
            <tr>
                <td>Lebih aman</td>
                <td>Tidak ada failover otomatis</td>
            </tr>
            <tr>
                <td>Tidak pakai bandwidth update</td>
                <td>Rawan human error</td>
            </tr>
        </table>
    </div>

    <div class="card">
        <h2>2. Dynamic Routing (Routing Dinamis)</h2>
        <p>
            Dynamic Routing adalah routing otomatis menggunakan protokol untuk bertukar informasi antar router.
        </p>

        <h3>Karakteristik:</h3>
        <ul>
            <li>Otomatis: Router saling bertukar informasi</li>
            <li>Adaptif: Bisa mencari jalur alternatif</li>
            <li>Skalabel: Cocok untuk jaringan besar</li>
        </ul>

        <h3>Protokol Populer:</h3>
        <ul>
            <li>RIP</li>
            <li>OSPF</li>
            <li>EIGRP</li>
            <li>BGP</li>
        </ul>

        <h3>Kelebihan & Kekurangan:</h3>
        <table>
            <tr>
                <th>Kelebihan</th>
                <th>Kekurangan</th>
            </tr>
            <tr>
                <td>Mudah untuk jaringan besar</td>
                <td>Menggunakan CPU & RAM</td>
            </tr>
            <tr>
                <td>Konvergensi cepat</td>
                <td>Butuh bandwidth</td>
            </tr>
            <tr>
                <td>Konfigurasi lebih sederhana</td>
                <td>Keamanan lebih rendah</td>
            </tr>
        </table>
    </div>

    <div class="card">
        <h2>3. Perbandingan Static vs Dynamic</h2>
        <table>
            <tr>
                <th>Fitur</th>
                <th>Static</th>
                <th>Dynamic</th>
            </tr>
            <tr>
                <td>Konfigurasi</td>
                <td>Manual</td>
                <td>Otomatis</td>
            </tr>
            <tr>
                <td>Skalabilitas</td>
                <td>Kecil</td>
                <td>Besar</td>
            </tr>
            <tr>
                <td>CPU/RAM</td>
                <td>Rendah</td>
                <td>Tinggi</td>
            </tr>
            <tr>
                <td>Bandwidth</td>
                <td>Tidak ada</td>
                <td>Ada</td>
            </tr>
            <tr>
                <td>Keamanan</td>
                <td>Tinggi</td>
                <td>Tergantung</td>
            </tr>
            <tr>
                <td>Adaptasi</td>
                <td>Tidak otomatis</td>
                <td>Otomatis</td>
            </tr>
        </table>
    </div>

    <div class="card">
        <h2>4. Kapan Digunakan?</h2>
        <p><b>Static Routing:</b> digunakan untuk jaringan kecil dan kontrol penuh.</p>
        <p><b>Dynamic Routing:</b> digunakan untuk jaringan besar dan topologi yang sering berubah.</p>

        <p><b>Catatan:</b> Dalam praktik nyata sering digunakan metode Hybrid.</p>
    </div>

</div>

</body>
</html>
