# PopaJoppa.github.io
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Тест по финансовой грамотности | Защита от мошенничества</title>
    <meta name="description" content="Проверьте свои знания в области финансов и узнайте, как защититься от мошенников">
    <style>
        :root {
            --primary: #2E8B57;
            --secondary: #228B22;
            --success: #32CD32;
            --warning: #FF8C00;
            --danger: #DC143C;
            --light: #f8f9fa;
            --dark: #212529;
            --border-radius: 10px;
            --box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #2E8B57 0%, #228B22 100%);
            color: #333;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            background: white;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--box-shadow);
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .card {
            padding: 30px;
        }
        
        .step {
            display: none;
        }
        
        .step.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        h2 {
            color: var(--dark);
            margin-bottom: 25px;
            border-bottom: 2px solid #f0f0f0;
            padding-bottom: 10px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark);
        }
        
        input, select {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: all 0.3s;
        }
        
        input:focus, select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(46, 139, 87, 0.1);
        }
        
        .question {
            margin-bottom: 25px;
            padding: 20px;
            border: 1px solid #eaeaea;
            border-radius: 10px;
            background: #fafafa;
        }
        
        .question-text {
            font-size: 1.1rem;
            margin-bottom: 15px;
            font-weight: 600;
            color: var(--dark);
        }
        
        .options {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        
        .option {
            display: flex;
            align-items: center;
            padding: 12px 15px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s;
            background: white;
        }
        
        .option:hover {
            border-color: var(--primary);
            background: #f0fff0;
        }
        
        .option.selected {
            background: #e8f5e8;
            border-color: var(--primary);
        }
        
        .option input {
            margin-right: 12px;
            width: auto;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 14px 30px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s;
            text-align: center;
            text-decoration: none;
        }
        
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn-container {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
            gap: 15px;
        }
        
        .btn-next {
            margin-left: auto;
        }
        
        .btn-prev {
            background: #6c757d;
        }
        
        .btn-prev:hover {
            background: #5a6268;
        }
        
        .progress-container {
            margin-bottom: 30px;
        }
        
        .progress-text {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }
        
        .progress-bar {
            height: 10px;
            background-color: #e9ecef;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--success));
            width: 0%;
            transition: width 0.5s ease;
        }
        
        .result-card {
            text-align: center;
            padding: 40px 30px;
        }
        
        .level {
            font-size: 2.2rem;
            margin: 20px 0;
            color: var(--primary);
            font-weight: 700;
        }
        
        .score {
            font-size: 1.5rem;
            margin: 15px 0;
            color: var(--success);
        }
        
        .description {
            margin-bottom: 30px;
            font-size: 1.1rem;
            line-height: 1.7;
        }
        
        .recommendations {
            text-align: left;
            margin-top: 30px;
            background: #f8f9fa;
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid var(--primary);
        }
        
        .recommendations h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .recommendations ul {
            padding-left: 20px;
        }
        
        .recommendations li {
            margin-bottom: 10px;
            line-height: 1.5;
        }
        
        .restart-btn {
            margin-top: 25px;
            background: var(--success);
        }
        
        .restart-btn:hover {
            background: #28a428;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #6c757d;
            font-size: 0.9rem;
            border-top: 1px solid #eaeaea;
        }
        
        .info-box {
            background: #e8f5e8;
            border: 1px solid #b8e0b8;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
        }
        
        .warning-box {
            background: #fff3e8;
            border: 1px solid #ffd9b8;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            border-left: 4px solid var(--warning);
        }
        
        .danger-box {
            background: #ffe8e8;
            border: 1px solid #ffb8b8;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            border-left: 4px solid var(--danger);
        }
        
        .subject-icon {
            font-size: 1.5rem;
            margin-right: 10px;
        }
        
        @media (max-width: 600px) {
            body {
                padding: 10px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .card {
                padding: 20px 15px;
            }
            
            .btn-container {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Финансовая грамотность и защита от мошенников</h1>
            <p class="subtitle">Проверьте свои знания и узнайте, как защитить свои финансы от мошенников</p>
        </header>
        
        <div class="card">
            <div class="progress-container">
                <div class="progress-text">
                    <span>Прогресс</span>
                    <span id="progress-percent">0%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress" id="progress"></div>
                </div>
            </div>
            
            <div class="step active" id="step1">
                <div class="info-box">
                    <p>💰 Этот тест поможет оценить ваш уровень финансовой грамотности и знание способов защиты от мошенников. Ответьте честно на все вопросы для получения точного результата и полезных рекомендаций.</p>
                </div>
                
                <h2>Информация о себе</h2>
                <div class="form-group">
                    <label for="name">Имя:</label>
                    <input type="text" id="name" placeholder="Введите ваше имя">
                </div>
                <div class="form-group">
                    <label for="age">Возрастная группа:</label>
                    <select id="age">
                        <option value="">Выберите возраст</option>
                        <option value="teen">До 18 лет</option>
                        <option value="young">18-25 лет</option>
                        <option value="adult">26-40 лет</option>
                        <option value="middle">41-60 лет</option>
                        <option value="senior">Старше 60 лет</option>
                    </select>
                </div>
                <div class="btn-container">
                    <button class="btn btn-next" id="start-btn">Начать тест</button>
                </div>
            </div>
            
            <div class="step" id="step2">
                <h2><span class="subject-icon">💰</span> Основы финансовой грамотности</h2>
                
                <div class="question">
                    <div class="question-text">1. Что такое инфляция?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q1" value="a"> Увеличение стоимости ценных бумаг
                        </label>
                        <label class="option">
                            <input type="radio" name="q1" value="b"> Повышение общего уровня цен на товары и услуги
                        </label>
                        <label class="option">
                            <input type="radio" name="q1" value="c"> Увеличение заработной платы
                        </label>
                        <label class="option">
                            <input type="radio" name="q1" value="d"> Снижение курса национальной валюты
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">2. Что такое "финансовая подушка безопасности"?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q2" value="a"> Деньги на развлечения
                        </label>
                        <label class="option">
                            <input type="radio" name="q2" value="b"> Сбережения на крупную покупку
                        </label>
                        <label class="option">
                            <input type="radio" name="q2" value="c"> Резерв средств на непредвиденные расходы
                        </label>
                        <label class="option">
                            <input type="radio" name="q2" value="d"> Деньги на инвестиции
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">3. Что такое сложный процент?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q3" value="a"> Процент, начисляемый только на первоначальную сумму
                        </label>
                        <label class="option">
                            <input type="radio" name="q3" value="b"> Высокий процент по вкладу
                        </label>
                        <label class="option">
                            <input type="radio" name="q3" value="c"> Процент, начисляемый на сумму с ранее начисленными процентами
                        </label>
                        <label class="option">
                            <input type="radio" name="q3" value="d"> Процент по кредиту
                        </label>
                    </div>
                </div>
                
                <div class="btn-container">
                    <button class="btn btn-prev" id="prev-btn-2">Назад</button>
                    <button class="btn btn-next" id="next-btn-2">Далее</button>
                </div>
            </div>
            
            <div class="step" id="step3">
                <h2><span class="subject-icon">🏦</span> Банковские продукты и безопасность</h2>
                
                <div class="question">
                    <div class="question-text">4. Что такое депозит?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q4" value="a"> Вид кредита
                        </label>
                        <label class="option">
                            <input type="radio" name="q4" value="b"> Вклад денежных средств в банк под проценты
                        </label>
                        <label class="option">
                            <input type="radio" name="q4" value="c"> Платежная карта
                        </label>
                        <label class="option">
                            <input type="radio" name="q4" value="d"> Страховой полис
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">5. Какие данные банковской карты можно сообщать по телефону?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q5" value="a"> Полный номер карты и CVV-код
                        </label>
                        <label class="option">
                            <input type="radio" name="q5" value="b"> Только номер карты
                        </label>
                        <label class="option">
                            <input type="radio" name="q5" value="c"> Никакие данные карты нельзя сообщать
                        </label>
                        <label class="option">
                            <input type="radio" name="q5" value="d"> Можно сообщить, если звонящий представился сотрудником банка
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">6. Что такое фишинг?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q6" value="a"> Вид рыбалки
                        </label>
                        <label class="option">
                            <input type="radio" name="q6" value="b"> Мошенническая схема с целью получения конфиденциальных данных
                        </label>
                        <label class="option">
                            <input type="radio" name="q6" value="c"> Вид инвестирования
                        </label>
                        <label class="option">
                            <input type="radio" name="q6" value="d"> Способ экономии денег
                        </label>
                    </div>
                </div>
                
                <div class="btn-container">
                    <button class="btn btn-prev" id="prev-btn-3">Назад</button>
                    <button class="btn btn-next" id="next-btn-3">Далее</button>
                </div>
            </div>
            
            <div class="step" id="step4">
                <h2><span class="subject-icon">🚫</span> Защита от мошенничества</h2>
                
                <div class="warning-box">
                    <p>⚠️ В этом разделе проверьте свои знания о способах защиты от финансовых мошенников.</p>
                </div>
                
                <div class="question">
                    <div class="question-text">7. Что делать, если вам позвонили и представились сотрудником банка, запрашивая данные карты?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q7" value="a"> Назвать данные, так как звонят из банка
                        </label>
                        <label class="option">
                            <input type="radio" name="q7" value="b"> Перезвонить в банк по официальному номеру для уточнения информации
                        </label>
                        <label class="option">
                            <input type="radio" name="q7" value="c"> Сообщить данные, но только номер карты
                        </label>
                        <label class="option">
                            <input type="radio" name="q7" value="d"> Ничего не делать, это точно мошенники
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">8. Как отличить финансовую пирамиду от легальной инвестиционной компании?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q8" value="a"> По наличию лицензии у компании
                        </label>
                        <label class="option">
                            <input type="radio" name="q8" value="b"> По обещаниям очень высокой доходности
                        </label>
                        <label class="option">
                            <input type="radio" name="q8" value="c"> По требованию привлекать новых участников для получения дохода
                        </label>
                        <label class="option">
                            <input type="radio" name="q8" value="d"> Все вышеперечисленное
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">9. Что такое "социальная инженерия" в контексте мошенничества?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q9" value="a"> Методы воздействия на людей для получения конфиденциальной информации
                        </label>
                        <label class="option">
                            <input type="radio" name="q9" value="b"> Инженерные работы в социальной сфере
                        </label>
                        <label class="option">
                            <input type="radio" name="q9" value="c"> Социальные программы помощи
                        </label>
                        <label class="option">
                            <input type="radio" name="q9" value="d"> Вид благотворительности
                        </label>
                    </div>
                </div>
                
                <div class="question">
                    <div class="question-text">10. Какие меры защиты следует предпринять при онлайн-покупках?</div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q10" value="a"> Покупать только на проверенных сайтах с HTTPS-протоколом
                        </label>
                        <label class="option">
                            <input type="radio" name="q10" value="b"> Использовать виртуальные карты для онлайн-платежей
                        </label>
                        <label class="option">
                            <input type="radio" name="q10" value="c"> Не сохранять данные карты на сайтах
                        </label>
                        <label class="option">
                            <input type="radio" name="q10" value="d"> Все вышеперечисленное
                        </label>
                    </div>
                </div>
                
                <div class="btn-container">
                    <button class="btn btn-prev" id="prev-btn-4">Назад</button>
                    <button class="btn btn-next" id="next-btn-4">Завершить тест</button>
                </div>
            </div>
            
            <div class="step" id="step5">
                <div class="result-card">
                    <h2>Результаты тестирования</h2>
                    <p id="student-info"></p>
                    <div class="score" id="score-result"></div>
                    <div class="level" id="level-result"></div>
                    <div class="description" id="level-description"></div>
                    
                    <div class="recommendations">
                        <h3>Рекомендации для улучшения финансовой грамотности и защиты от мошенников:</h3>
                        <ul id="recommendations-list"></ul>
                    </div>
                    
                    <div class="danger-box">
                        <h3>⚠️ Важные правила безопасности:</h3>
                        <ul>
                            <li>Никогда не сообщайте никому PIN-код, CVV-код и полные данные карты</li>
                            <li>Установите лимиты на онлайн-операции в мобильном приложении банка</li>
                            <li>Включайте двухфакторную аутентификацию для всех финансовых сервисов</li>
                            <li>Регулярно проверяйте выписки по картам и счетам</li>
                        </ul>
                    </div>
                    
                    <button class="btn restart-btn" id="restart-btn">Пройти тест заново</button>
                </div>
            </div>
        </div>
        
        <footer>
            <p>© 2023 Тест по финансовой грамотности и защите от мошенников. Бесплатный онлайн-опросник.</p>
        </footer>
    </div>

    <script>
        // Правильные ответы
        const correctAnswers = {
            q1: 'b',
            q2: 'c',
            q3: 'c',
            q4: 'b',
            q5: 'c',
            q6: 'b',
            q7: 'b',
            q8: 'd',
            q9: 'a',
            q10: 'd'
        };
        
        // Описания уровней
        const levelDescriptions = {
            beginner: {
                name: "Начальный уровень",
                description: "У вас есть базовые представления о финансах, но много важных аспектов требуют изучения. Особенно важно изучить способы защиты от мошенников.",
                recommendations: [
                    "Изучите основы финансовой грамотности: бюджет, сбережения, кредиты",
                    "Научитесь распознавать основные схемы финансового мошенничества",
                    "Создайте финансовую подушку безопасности на 3-6 месяцев",
                    "Никогда не сообщайте данные карты по телефону или в сообщениях",
                    "Установите мобильное приложение банка и настройте уведомления о операциях"
                ]
            },
            intermediate: {
                name: "Средний уровень",
                description: "У вас хорошие базовые знания в области финансов, но есть темы, которые требуют углубленного изучения, особенно в области кибербезопасности.",
                recommendations: [
                    "Углубите знания в области защиты от финансового мошенничества",
                    "Используйте виртуальные карты для онлайн-платежей",
                    "Включите двухфакторную аутентификацию для всех финансовых сервисов",
                    "Регулярно проверяйте свою кредитную историю",
                    "Изучите возможности страхования финансовых рисков"
                ]
            },
            advanced: {
                name: "Продвинутый уровень",
                description: "Поздравляем! У вас отличные знания в области финансов и защиты от мошенников. Вы понимаете основные финансовые концепции и способы защиты.",
                recommendations: [
                    "Продолжайте следить за новыми схемами мошенничества",
                    "Обучайте близких правилам финансовой безопасности",
                    "Рассмотрите возможности для диверсификации инвестиционного портфеля",
                    "Используйте отдельные карты для разных типов операций",
                    "Регулярно обновляйте пароли к финансовым сервисам"
                ]
            }
        };
        
        let currentStep = 1;
        const totalSteps = 5;
        
        // Функция обновления прогресс-бара
        function updateProgress() {
            const progress = document.getElementById('progress');
            const progressPercent = document.getElementById('progress-percent');
            const percentage = ((currentStep - 1) / (totalSteps - 1)) * 100;
            progress.style.width = percentage + '%';
            progressPercent.textContent = Math.round(percentage) + '%';
        }
        
        // Функция перехода к следующему шагу
        function nextStep() {
            // Проверка заполнения текущего шага
            if (currentStep === 1) {
                const name = document.getElementById('name').value;
                const age = document.getElementById('age').value;
                
                if (!name || !age) {
                    alert('Пожалуйста, заполните все поля');
                    return;
                }
            } else {
                // Проверка ответов на вопросы текущего шага
                let allAnswered = true;
                const questions = document.querySelectorAll(`#step${currentStep} input[type="radio"]`);
                const questionGroups = {};
                
                questions.forEach(q => {
                    const name = q.getAttribute('name');
                    if (!questionGroups[name]) questionGroups[name] = [];
                    questionGroups[name].push(q);
                });
                
                for (const group in questionGroups) {
                    let answered = false;
                    questionGroups[group].forEach(q => {
                        if (q.checked) answered = true;
                    });
                    if (!answered) allAnswered = false;
                }
                
                if (!allAnswered) {
                    alert('Пожалуйста, ответьте на все вопросы перед переходом к следующему шагу');
                    return;
                }
            }
            
            // Переход к следующему шагу
            document.getElementById(`step${currentStep}`).classList.remove('active');
            currentStep++;
            document.getElementById(`step${currentStep}`).classList.add('active');
            updateProgress();
            
            // Если это последний шаг, показать результаты
            if (currentStep === totalSteps) {
                showResults();
            }
        }
        
        // Функция перехода к предыдущему шагу
        function prevStep() {
            document.getElementById(`step${currentStep}`).classList.remove('active');
            currentStep--;
            document.getElementById(`step${currentStep}`).classList.add('active');
            updateProgress();
        }
        
        // Функция показа результатов
        function showResults() {
            // Сбор информации о пользователе
            const name = document.getElementById('name').value;
            const age = document.getElementById('age').value;
            const ageLabels = {
                'teen': 'До 18 лет',
                'young': '18-25 лет',
                'adult': '26-40 лет',
                'middle': '41-60 лет',
                'senior': 'Старше 60 лет'
            };
            document.getElementById('student-info').textContent = `${name}, ${ageLabels[age]}`;
            
            // Подсчет правильных ответов
            let score = 0;
            const totalQuestions = Object.keys(correctAnswers).length;
            
            for (const question in correctAnswers) {
                const selected = document.querySelector(`input[name="${question}"]:checked`);
                if (selected && selected.value === correctAnswers[question]) {
                    score++;
                }
            }
            
            // Определение уровня
            let level;
            if (score <= 4) {
                level = 'beginner';
            } else if (score <= 7) {
                level = 'intermediate';
            } else {
                level = 'advanced';
            }
            
            // Отображение результатов
            document.getElementById('score-result').textContent = `Правильных ответов: ${score} из ${totalQuestions}`;
            document.getElementById('level-result').textContent = levelDescriptions[level].name;
            document.getElementById('level-description').textContent = levelDescriptions[level].description;
            
            const recommendationsList = document.getElementById('recommendations-list');
            recommendationsList.innerHTML = '';
            levelDescriptions[level].recommendations.forEach(rec => {
                const li = document.createElement('li');
                li.textContent = rec;
                recommendationsList.appendChild(li);
            });
        }
        
        // Функция перезапуска теста
        function restartTest() {
            // Сброс формы
            document.getElementById('name').value = '';
            document.getElementById('age').value = '';
            
            // Сброс выбранных ответов
            const allInputs = document.querySelectorAll('input[type="radio"]');
            allInputs.forEach(input => {
                input.checked = false;
                input.parentElement.classList.remove('selected');
            });
            
            // Возврат к первому шагу
            document.getElementById(`step${currentStep}`).classList.remove('active');
            currentStep = 1;
            document.getElementById(`step${currentStep}`).classList.add('active');
            updateProgress();
            
            // Прокрутка к верху страницы
            window.scrollTo(0, 0);
        }
        
        // Инициализация после загрузки DOM
        document.addEventListener('DOMContentLoaded', function() {
            // Обработчики для вариантов ответов
            const options = document.querySelectorAll('.option');
            options.forEach(option => {
                option.addEventListener('click', function() {
                    const radio = this.querySelector('input[type="radio"]');
                    radio.checked = true;
                    
                    // Снимаем выделение со всех вариантов в группе
                    const groupName = radio.getAttribute('name');
                    const groupOptions = document.querySelectorAll(`input[name="${groupName}"]`);
                    groupOptions.forEach(opt => {
                        opt.parentElement.classList.remove('selected');
                    });
                    
                    // Выделяем выбранный вариант
                    this.classList.add('selected');
                });
            });
            
            // Обработчики для кнопок навигации
            document.getElementById('start-btn').addEventListener('click', nextStep);
            document.getElementById('next-btn-2').addEventListener('click', nextStep);
            document.getElementById('next-btn-3').addEventListener('click', nextStep);
            document.getElementById('next-btn-4').addEventListener('click', nextStep);
            
            document.getElementById('prev-btn-2').addEventListener('click', prevStep);
            document.getElementById('prev-btn-3').addEventListener('click', prevStep);
            document.getElementById('prev-btn-4').addEventListener('click', prevStep);
            
            document.getElementById('restart-btn').addEventListener('click', restartTest);
            
            // Инициализация прогресс-бара
            updateProgress();
        });
    </script>
</body>
</html>
