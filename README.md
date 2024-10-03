<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentasi Sejarah Jong Sumatran Bond</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        #container {
            width: 80%;
            max-width: 900px;
            background-color: white;
            box-shadow: 0px 0px 15px rgba(0,0,0,0.1);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }
        .slide {
            display: none;
        }
        .slide.active {
            display: block;
        }
        .slide img {
            max-width: 100%;
            height: auto;
            margin-top: 20px;
        }
        .controls {
            text-align: center;
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 0 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

    <div id="container">
        <!-- Slide 1 -->
        <div class="slide active">
            <h1>Sejarah Jong Sumatran Bond</h1>
            <p>Jong Sumatran Bond adalah organisasi pemuda yang didirikan oleh para pelajar asal Sumatera pada tahun 1917.</p>
            <img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/Jong_Sumatranen_Bond_logo.png" alt="Logo Jong Sumatran Bond">
        </div>

        <!-- Slide 2 -->
        <div class="slide">
            <h2>Pendirian Jong Sumatran Bond</h2>
            <p>Jong Sumatran Bond didirikan pada 9 Desember 1917 di Batavia. Organisasi ini bertujuan untuk mempersatukan pemuda Sumatera.</p>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Logo_Sumpah_Pemuda.png/800px-Logo_Sumpah_Pemuda.png" alt="Sumpah Pemuda">
        </div>

        <!-- Slide 3 -->
        <div class="slide">
            <h2>Tujuan Jong Sumatran Bond</h2>
            <p>Jong Sumatran Bond berfokus pada persatuan pemuda Sumatera dan memajukan pendidikan serta kebudayaan Sumatera.</p>
            <img src="https://upload.wikimedia.org/wikipedia/commons/5/54/Sumpah_Pemuda_Museum.jpg" alt="Museum Sumpah Pemuda">
        </div>

        <!-- Slide 4 -->
        <div class="slide">
            <h2>Peran dalam Pergerakan Nasional</h2>
            <p>Jong Sumatran Bond berperan penting dalam pergerakan nasional, terutama dengan keterlibatannya dalam Kongres Pemuda II pada tahun 1928.</p>
            <img src="https://upload.wikimedia.org/wikipedia/commons/0/04/Kongres_Pemuda_Indonesia.jpg" alt="Kongres Pemuda II">
        </div>

        <!-- Slide 5 -->
        <div class="slide">
            <h2>Pembubaran</h2>
            <p>Setelah Sumpah Pemuda, Jong Sumatran Bond bergabung dengan organisasi pemuda lainnya dan menjadi bagian dari gerakan nasional.</p>
            <img src="https://upload.wikimedia.org/wikipedia/commons/6/6a/Bendera_Merah_Putih.png" alt="Bendera Merah Putih">
        </div>

        <!-- Control buttons -->
        <div class="controls">
            <button id="prevBtn">Sebelumnya</button>
            <button id="nextBtn">Berikutnya</button>
        </div>
    </div>

    <script>
        const slides = document.querySelectorAll('.slide');
        let currentSlide = 0;

        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');

        function showSlide(index) {
            slides.forEach((slide, i) => {
                if (i === index) {
                    slide.classList.add('active');
                } else {
                    slide.classList.remove('active');
                }
            });
        }

        nextBtn.addEventListener('click', () => {
            if (currentSlide < slides.length - 1) {
                currentSlide++;
            }
            showSlide(currentSlide);
        });

        prevBtn.addEventListener('click', () => {
            if (currentSlide > 0) {
                currentSlide--;
            }
            showSlide(currentSlide);
        });
    </script>

</body>
</html>
