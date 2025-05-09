      return;
    }
    const reportData = {
      "Ваш ник": form.yourNick.value.trim(),
      "Ник нарушителя": form.offenderNick.value.trim(),
      "Причина": form.reason.value,
      "Доказательство": form.proof.value.trim()
    };
    let reportText = "Отчет для администрации Chill Hangout:\n\n";
    for(const [key, val] of Object.entries(reportData)) {
      reportText += `${key}: ${val}\n`;
    }
    if(confirm("Отчет сформирован! Скопировать отчет в буфер обмена для отправки?")) {
      navigator.clipboard.writeText(reportText).then(() => {
        alert("Отчет скопирован в буфер обмена.\nТеперь вставьте его в личные сообщения администрации или нужный канал.");
        form.reset();
      }, () => {
        alert("Не удалось скопировать автоматически, пожалуйста скопируйте вручную:\n\n" + reportText);
      });
    } else {
      alert("Отчет сформирован:\n\n" + reportText);
    }
  });
</script>
</body>
</html>
            font-size: 0.9rem;
            font-family: 'Inter', sans-serif;
            resize: vertical;
            background: #47376b;
            color: #e9dbff;
            transition: background-color 0.3s ease;
        }
        input[type="text"]:focus,
        select:focus,
        textarea:focus {
            outline: none;
            background: #5a4691;
        }
        textarea {
            min-height: 80px;
        }
        button {
            width: 100%;
            background: #ab47bc;
            border: none;
            padding: 12px;
            border-radius: 10px;
            color: white;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 4px 10px #9c27b0;
            transition: background-color 0.3s ease;
            margin-top: 15px;
        .container::-webkit-scrollbar-track {
            background: #2e1a47dd;
        }
        .container::-webkit-scrollbar-thumb {
            background: #7b1fa2cc;
            border-radius: 10px;
        }
        @media (max-width: 400px) {
            body {
                padding: 5px;
            }
            .container {
        }
        textarea {
            min-height: 80px;
        }
        button {
            width: 100%;
            background: #ab47bc;
            border: none;
            padding: 12px;
            border-radius: 10px;
            color: white;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 4px 10px #9c27b0;
            transition: background-color 0.3s ease;
            margin-top: 15px;
      <option value="другое">Другое</option>
    </select>
    <label for="proof">Доказательство (ссылка или описание)</label>
    <textarea id="proof" name="proof" placeholder="Вставьте ссылку на скриншот, видео или опишите ситуацию" required minlength="10"></textarea>
    <button type="submit">Отправить</button>
  </form>
<script>
  const form = document.getElementById('reportForm');
            background: #2e1a47dd;
        }
        .container::-webkit-scrollbar-thumb {
            background: #7b1fa2cc;
            border-radius: 10px;
        }
        @media (max-width: 400px) {
            body {
                padding: 5px;
            }
            .container {
                max-width: 100vw;
                max-height: 100vh;
                border-radius: 0;
            }
        }
    </style>
</head>
<body>
  <form class="container" id="reportForm" novalidate>
    <h1>Отчет для администрации Chill Hangout</h1>
    <label for="yourNick">Ваш ник (с тегом, например Example#1234)</label>
    <input type="text" id="yourNick" name="yourNick" placeholder="Example#1234" required pattern=".+#\d{4}$" title="Никнейм должен содержать # и 4 цифры" />
    <label for="offenderNick">Ник нарушителя (с тегом, например BadUser#9999)</label>
    <input type="text" id="offenderNick" name="offenderNick" placeholder="BadUser#9999" required pattern=".+#\d{4}$" title="Никнейм должен содержать # и 4 цифры" />
    <label for="reason">Причина</label>
    <select id="reason" name="reason" required>
      <option value="">Выберите причину</option>
      <option value="спам">Спам</option>
      <option value="оскорбления">Оскорбления</option>
      <option value="читерство">Читерство</option>
      <option value="реклама">Реклама</option>
      <option value="другое">Другое</option>
    </select>
      <option value="другое">Другое</option>
    </select>
    <label for="proof">Доказательство (ссылка или описание)</label>
    <textarea id="proof" name="proof" placeholder="Вставьте ссылку на скриншот, видео или опишите ситуацию" required minlength="10"></textarea>
    <button type="submit">Отправить</button>
  </form>
<script>
  const form = document.getElementById('reportForm');
  form.addEventListener('submit', e => {
    e.preventDefault();
    if(!form.checkValidity()) {
      form.reportValidity();
      return;
    }
    const reportData = {
      "Ваш ник": form.yourNick.value.trim(),
      "Ник нарушителя": form.offenderNick.value.trim(),
      "Причина": form.reason.value,
      "Доказательство": form.proof.value.trim()
    };
    let reportText = "Отчет для администрации Chill Hangout:\n\n";
    for(const [key, val] of Object.entries(reportData)) {
      reportText += `${key}: ${val}\n`;
    }
    if(confirm("Отчет сформирован! Скопировать отчет в буфер обмена для отправки?")) {
      navigator.clipboard.writeText(reportText).then(() => {
        alert("Отчет скопирован в буфер обмена.\nТеперь вставьте его в личные сообщения администрации или нужный канал.");
        form.reset();
      }, () => {
        alert("Не удалось скопировать автоматически, пожалуйста скопируйте вручную:\n\n" + reportText);
      });
    } else {
    alert("Отчет сформирован:\n\n" + reportText);
    }
  });
</script>
</body>
</html>
