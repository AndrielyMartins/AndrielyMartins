## Hi 😄
<?php
// Array com suas habilidades e o nível de domínio (0 a 100%)
$habilidades = [
    "PHP" => 85,
    "HTML5 & CSS3" => 90,
    "JavaScript" => 75,
    "MySQL / Banco de Dados" => 80,
    "Git & GitHub" => 70
];
?>

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minhas Habilidades</title>
    <!-- CSS do Bootstrap para estilização rápida -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light py-5">

    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8 bg-white p-4 rounded shadow-sm">
                <h2 class="mb-4 text-center">Minhas Habilidades Tecnica</h2>
                
                <?php foreach ($habilidades as $nome => $porcentagem): ?>
                    <div class="mb-3">
                        <div class="d-flex justify-content-between mb-1">
                            <span class="fw-bold"><?php echo htmlspecialchars($nome); ?></span>
                            <span><?php echo $porcentagem; ?>%</span>
                        </div>
                        <div class="progress" role="progressbar" aria-valuenow="<?php echo $porcentagem; ?>" aria-valuemin="0" aria-valuemax="100">
                            <div class="progress-bar bg-primary" style="width: <?php echo $porcentagem; ?>%"></div>
                        </div>
                    </div>
                <?php endforeach; ?>

            </div>
        </div>
    </div>

</body>
</html>
