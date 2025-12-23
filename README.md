# Huyen_Speaking_201-300
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Luyện Từ Vựng Daily Life - Red Edition Pro</title>
    <style>
        :root {
            --primary-color: #d32f2f;
            --secondary-color: #b71c1c;
            --accent-light: #ffebee;
            --bg-color: #fdf2f2;
            --card-bg: #ffffff;
            --text-color: #333333;
            --success-color: #2e7d32;
            --warning-color: #f57f17;
            --gray-color: #757575;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            color: var(--text-color);
            padding: 10px;
            box-sizing: border-box;
        }

        .container {
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(211, 47, 47, 0.15);
            width: 100%;
            max-width: 600px;
            text-align: center;
            border-top: 5px solid var(--primary-color);
            position: relative;
            box-sizing: border-box;
        }

        /* Header & Progress */
        .header-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .header-controls {
            display: flex;
            gap: 10px;
        }

        .btn-icon {
            background: none;
            border: none;
            font-size: 22px; 
            cursor: pointer;
            color: var(--primary-color);
            padding: 5px;
            transition: transform 0.2s;
        }
        .btn-icon:hover { transform: scale(1.1); }

        .progress-bar {
            color: #ef5350;
            font-weight: 600;
            font-size: 14px;
            letter-spacing: 1px;
        }

        /* Card Area */
        .card {
            min-height: 300px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            padding: 10px;
        }

        .vietnamese-text {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #2c3e50;
            line-height: 1.4;
            word-wrap: break-word; 
        }

        .hidden-content {
            display: none;
            animation: fadeIn 0.5s ease-out;
            width: 100%;
        }

        .english-row {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin: 10px 0;
            flex-wrap: wrap;
        }

        .english-word {
            font-size: 28px;
            color: var(--primary-color);
            font-weight: 800;
            text-shadow: 1px 1px 0px rgba(0,0,0,0.05);
            margin: 0;
            word-break: break-word; 
            line-height: 1.3;
        }

        .ipa-text {
            font-family: 'Lucida Sans Unicode', 'Arial Unicode MS', sans-serif;
            font-size: 18px;
            color: #757575;
            margin-bottom: 15px;
            font-weight: 400;
        }

        .btn-audio-replay {
            background: white;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            width: 40px; 
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
            flex-shrink: 0;
            -webkit-tap-highlight-color: transparent; 
        }
        .btn-audio-replay:hover {
            background: var(--primary-color);
            color: white;
            transform: scale(1.1);
        }

        .part-of-speech {
            font-style: italic;
            color: #c62828;
            margin-bottom: 8px;
            font-size: 14px;
            background: var(--accent-light);
            padding: 5px 12px;
            border-radius: 15px;
            display: inline-block;
            border: 1px solid #ffcdd2;
        }

        .example-box {
            font-size: 16px;
            color: #4b5563;
            margin-top: 15px;
            padding: 15px;
            background-color: #fff5f5;
            border-left: 4px solid var(--primary-color);
            border-radius: 0 8px 8px 0;
            text-align: left;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            line-height: 1.5;
            display: none; 
        }

        /* Buttons */
        .btn {
            border: none;
            padding: 14px 20px; 
            font-size: 16px;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            color: white;
            -webkit-tap-highlight-color: transparent;
        }
        
        .btn:hover { transform: translateY(-2px); box-shadow: 0 6px 12px rgba(0,0,0,0.15); }
        .btn:active { transform: translateY(1px); }
        .btn:disabled { background: #bdbdbd !important; cursor: not-allowed; transform: none; box-shadow: none; color: #fff;}

        .btn-reveal {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            width: 100%;
            margin-top: 20px;
            font-size: 18px;
        }

        .nav-row {
            display: flex;
            justify-content: space-between;
            margin-top: 25px;
            gap: 15px;
        }

        .btn-nav {
            background-color: white;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
            width: 55px; 
            height: 55px;
            border-radius: 50%;
            font-size: 22px;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 0;
        }

        .review-actions {
            display: flex;
            gap: 10px;
            margin-top: 20px;
            justify-content: center;
        }

        .btn-learn { background-color: var(--warning-color); flex: 1; }
        .btn-success { background-color: var(--success-color); flex: 1; }

        .status-badge {
            font-size: 12px;
            padding: 4px 8px;
            border-radius: 4px;
            margin-bottom: 10px;
            display: inline-block;
            font-weight: bold;
        }
        .status-new { color: var(--gray-color); background: #eee; }
        .status-learned { color: var(--success-color); background: #e8f5e9; border: 1px solid #c8e6c9; }
        .status-learning { color: var(--warning-color); background: #fff3e0; border: 1px solid #ffe0b2; }

        .status-msg {
            font-size: 13px;
            margin-top: 10px;
            color: #e53935;
            font-style: italic;
            height: 20px;
        }

        /* Modal Global */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.6);
            z-index: 100;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(2px);
        }

        .modal-content {
            background: white;
            width: 90%;
            max-width: 400px;
            max-height: 85vh; 
            border-radius: 15px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 20px 50px rgba(0,0,0,0.3);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }

        .list-container {
            overflow-y: auto;
            flex: 1;
            -webkit-overflow-scrolling: touch; 
        }

        .list-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 10px; 
            border-bottom: 1px solid #f5f5f5;
            cursor: pointer;
            text-align: left;
            align-items: center;
        }
        .list-item:hover { background-color: #fce4ec; }
        .list-item.active { background-color: #ffcdd2; font-weight: bold; }

        .stats-summary {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
            text-align: center;
        }
        .stat-box {
            padding: 10px;
            border-radius: 10px;
            width: 30%;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .stat-val { font-size: 20px; font-weight: bold; display: block; }
        .stat-label { font-size: 12px; }
        
        .bg-learned { background: #e8f5e9; color: var(--success-color); }
        .bg-learning { background: #fff3e0; color: var(--warning-color); }
        .bg-new { background: #f5f5f5; color: var(--gray-color); }

        .recommend-section {
            text-align: left;
            margin-top: 10px;
            flex: 1;
            overflow-y: auto;
            -webkit-overflow-scrolling: touch;
        }
        .recommend-item {
            padding: 12px 8px;
            border-bottom: 1px solid #eee;
            cursor: pointer;
            color: var(--warning-color);
            font-weight: 500;
        }
        .recommend-item:hover { background: #fff3e0; }
        
        .settings-row {
            margin-bottom: 15px;
            text-align: left;
        }
        .settings-label {
            font-weight: 600;
            margin-bottom: 5px;
            display: block;
            color: #555;
        }
        select.settings-input {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: 1px solid #ccc;
            font-size: 14px;
            background: #fff;
        }
        input[type=range] {
            width: 100%;
            margin-top: 5px;
        }

        @media (max-width: 480px) {
            .container { padding: 20px; }
            .vietnamese-text { font-size: 20px; }
            .english-word { font-size: 24px; }
            .card { min-height: 240px; }
            .btn { font-size: 15px; padding: 12px; }
            .btn-nav { width: 45px; height: 45px; font-size: 18px; }
            .header-controls { gap: 8px; }
            .btn-icon { font-size: 22px; }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header-row">
        <div class="header-controls">
            <button class="btn-icon" onclick="toggleList()" title="Danh sách từ">☰</button>
            <button class="btn-icon" onclick="toggleStats()" title="Thống kê">📊</button>
            <button class="btn-icon" onclick="toggleSettings()" title="Cài đặt âm thanh">⚙️</button>
            <button class="btn-icon" onclick="shuffleVocabulary()" title="Đảo thứ tự">🔀</button>
        </div>
        <div id="progress" class="progress-bar">CÂU 1 / 99</div>
    </div>

    <div id="current-status" class="status-badge status-new">Mới</div>
    
    <div class="card">
        <!-- Phần câu hỏi Tiếng Việt -->
        <div id="question-area">
            <div class="vietnamese-text" id="vn-text">Đang tải dữ liệu...</div>
        </div>

        <!-- Phần đáp án (Ẩn) -->
        <div id="answer-area" class="hidden-content">
            <div class="part-of-speech" id="pos-text"></div>
            
            <!-- Hàng chứa từ và loa -->
            <div class="english-row">
                <div class="english-word" id="en-text"></div>
                <button class="btn-audio-replay" onclick="playCurrentAudio()" title="Nghe lại">🔊</button>
            </div>
            
            <!-- Phiên âm IPA -->
            <div class="ipa-text" id="ipa-text"></div>
            
            <!-- Ví dụ (Nếu có) -->
            <div class="example-box" id="example-text"></div>
        </div>
    </div>

    <div id="status-msg" class="status-msg"></div>

    <div id="main-actions">
        <button id="btn-reveal" class="btn btn-reveal" onclick="revealAnswer()">XEM ĐÁP ÁN</button>
    </div>

    <div id="review-actions" class="review-actions" style="display: none;">
        <button class="btn btn-learn" onclick="markStatus('learning')">Chưa thuộc 😕</button>
        <button class="btn btn-success" onclick="markStatus('learned')">Đã thuộc 😎</button>
    </div>

    <div class="nav-row">
        <button class="btn btn-nav" onclick="changeCard(-1)">❮</button>
        <button class="btn btn-nav" onclick="changeCard(1)">❯</button>
    </div>
</div>

<!-- Modal Danh Sách -->
<div id="list-modal" class="modal-overlay">
    <div class="modal-content">
        <div class="modal-header">
            <h3 style="margin:0; color:var(--primary-color)">Danh Sách 99 Từ</h3>
            <button onclick="toggleList()" style="border:none; background:none; font-size:24px; cursor:pointer;">&times;</button>
        </div>
        <div class="list-container" id="vocab-list-content"></div>
    </div>
</div>

<!-- Modal Thống Kê -->
<div id="stats-modal" class="modal-overlay">
    <div class="modal-content">
        <div class="modal-header">
            <h3 style="margin:0; color:var(--primary-color)">Thống Kê Học Tập</h3>
            <button onclick="toggleStats()" style="border:none; background:none; font-size:24px; cursor:pointer;">&times;</button>
        </div>
        
        <div class="stats-summary">
            <div class="stat-box bg-learned">
                <span class="stat-val" id="stat-learned">0</span>
                <span class="stat-label">Đã thuộc</span>
            </div>
            <div class="stat-box bg-learning">
                <span class="stat-val" id="stat-learning">0</span>
                <span class="stat-label">Chưa thuộc</span>
            </div>
            <div class="stat-box bg-new">
                <span class="stat-val" id="stat-new">0</span>
                <span class="stat-label">Mới</span>
            </div>
        </div>

        <hr style="border:0; border-top:1px solid #eee; width:100%; margin: 10px 0;">
        <h4 style="margin: 0 0 10px 0; color: #555;">💡 Cần ôn tập ngay:</h4>
        <div class="recommend-section" id="recommend-list"></div>
    </div>
</div>

<!-- Modal Cài Đặt -->
<div id="settings-modal" class="modal-overlay">
    <div class="modal-content">
        <div class="modal-header">
            <h3 style="margin:0; color:var(--primary-color)">Cài Đặt Âm Thanh</h3>
            <button onclick="toggleSettings()" style="border:none; background:none; font-size:24px; cursor:pointer;">&times;</button>
        </div>
        
        <div style="padding: 10px 0;">
            <div class="settings-row">
                <label class="settings-label">Chọn Giọng Đọc (Hệ thống):</label>
                <select id="voice-select" class="settings-input" onchange="updateVoiceSettings()">
                    <option value="-1">Tự động chọn (Tốt nhất)</option>
                </select>
            </div>
            
            <div class="settings-row">
                <label class="settings-label">Tốc Độ Đọc: <span id="speed-display" style="color:var(--primary-color)">0.8</span></label>
                <input type="range" id="speed-range" min="0.4" max="1.5" step="0.1" value="0.8" oninput="updateSpeedSettings()">
                <div style="display:flex; justify-content:space-between; font-size:12px; color:#999; margin-top:5px;">
                    <span>Chậm (0.4)</span>
                    <span>Nhanh (1.5)</span>
                </div>
            </div>
            
            <button class="btn" style="width:100%; margin-top:10px;" onclick="testVoice()">🔊 Nghe thử</button>
        </div>
    </div>
</div>

<script>
    // === DỮ LIỆU TỪ VỰNG 99 CÂU ===
    const initialVocabulary = [
        { en: "On a daily basis", pos: "(adv phrase)", ipa: "/ɒn ə ˈdeɪ.li ˈbeɪ.sɪs/", vi: "Hàng ngày" },
        { en: "From time to time", pos: "(adv phrase)", ipa: "/frɒm taɪm tu taɪm/", vi: "Thỉnh thoảng" },
        { en: "Every now and then", pos: "(adv phrase)", ipa: "/ˈev.ri naʊ ənd ðen/", vi: "Thỉnh thoảng" },
        { en: "Frequently", pos: "(adv)", ipa: "/ˈfriː.kwənt.li/", vi: "Thường xuyên" },
        { en: "Hardly ever / Rarely", pos: "(adv)", ipa: "/ˈhɑːd.li ˈev.ər/ - /ˈreə.li/", vi: "Hiếm khi" },
        { en: "Make a habit of", pos: "(v phrase)", ipa: "/meɪk ə ˈhæb.ɪt əv/", vi: "Tạo thói quen làm gì" },
        { en: "Get into the habit of", pos: "(v phrase)", ipa: "/ɡet ˈɪn.tu ðə ˈhæb.ɪt əv/", vi: "Bắt đầu thói quen gì" },
        { en: "Kick the bad habit", pos: "(v phrase)", ipa: "/kɪk ðə bæd ˈhæb.ɪt/", vi: "Từ bỏ thói quen xấu" },
        { en: "Stick to a routine", pos: "(v phrase)", ipa: "/stɪk tu ə ruːˈtiːn/", vi: "Tuân thủ lịch trình/thói quen" },
        { en: "Tend to", pos: "(v phrase)", ipa: "/tend tu/", vi: "Có xu hướng" },
        { en: "Without fail", pos: "(idiom)", ipa: "/wɪˈðaʊt feɪl/", vi: "Không bao giờ bỏ sót (đều đặn)" },
        { en: "Early bird / Morning person", pos: "(n phrase)", ipa: "/ˈɜː.li bɜːd/", vi: "Người hay dậy sớm" },
        { en: "Wake up at the crack of dawn", pos: "(idiom)", ipa: "/weɪk ʌp æt ðə kræk əv dɔːn/", vi: "Dậy khi tờ mờ sáng" },
        { en: "Hit the snooze button", pos: "(v phrase)", ipa: "/hɪt ðə snuːz ˈbʌt.ən/", vi: "Bấm nút hoãn báo thức" },
        { en: "Oversleep", pos: "(v)", ipa: "/ˌəʊ.vəˈsliːp/", vi: "Ngủ quên" },
        { en: "Have a nutritious breakfast", pos: "(v phrase)", ipa: "/hæv ə njuːˈtrɪʃ.əs ˈbrek.fəst/", vi: "Ăn bữa sáng dinh dưỡng" },
        { en: "Skip breakfast", pos: "(v phrase)", ipa: "/skɪp ˈbrek.fəst/", vi: "Bỏ bữa sáng" },
        { en: "Grab a quick bite", pos: "(v phrase)", ipa: "/ɡræb ə kwɪk baɪt/", vi: "Ăn vội cái gì đó" },
        { en: "Get ready for school", pos: "(v phrase)", ipa: "/ɡet ˈred.i fɔː skuːl/", vi: "Chuẩn bị đi học" },
        { en: "Rush out the door", pos: "(v phrase)", ipa: "/rʌʃ aʊt ðə dɔːr/", vi: "Lao ra khỏi nhà" },
        { en: "Productive day", pos: "(n phrase)", ipa: "/prəˈdʌk.tɪv deɪ/", vi: "Một ngày năng suất" },
        { en: "Take a nap", pos: "(v phrase)", ipa: "/teɪk ə næp/", vi: "Ngủ trưa một chút" },
        { en: "Run errands", pos: "(v phrase)", ipa: "/rʌn ˈer.əndz/", vi: "Chạy việc vặt" },
        { en: "Stay hydrated", pos: "(v phrase)", ipa: "/steɪ ˈhaɪ.dreɪ.tɪd/", vi: "Uống đủ nước" },
        { en: "Wind down", pos: "(phrasal v)", ipa: "/waɪnd daʊn/", vi: "Thư giãn, xả hơi" },
        { en: "Scroll through social media", pos: "(v phrase)", ipa: "/skrəʊl θruː ˈsəʊ.ʃəl ˈmiː.di.ə/", vi: "Lướt mạng xã hội" },
        { en: "Binge-watch", pos: "(v)", ipa: "/ˈbɪndʒ.wɒtʃ/", vi: "Cày phim liên tục" },
        { en: "Call it a day", pos: "(idiom)", ipa: "/kɔːl ɪt ə deɪ/", vi: "Kết thúc ngày làm việc" },
        { en: "Stay up late", pos: "(v phrase)", ipa: "/steɪ ʌp leɪt/", vi: "Thức khuya" },
        { en: "Pull an all-nighter", pos: "(idiom)", ipa: "/pʊl ən ɔːl ˈnaɪ.tər/", vi: "Thức trắng đêm" },
        { en: "Have a lie-in / Sleep in", pos: "(v phrase)", ipa: "/hæv ə laɪ ɪn/", vi: "Ngủ nướng (chủ động)" },
        { en: "Recharge my batteries", pos: "(idiom)", ipa: "/riːˈtʃɑːdʒ maɪ ˈbæt.ər.iz/", vi: "Nạp lại năng lượng" },
        { en: "Let my hair down", pos: "(idiom)", ipa: "/let maɪ heər daʊn/", vi: "Xả hơi, quẩy" },
        { en: "Quality time", pos: "(n phrase)", ipa: "/ˈkwɒl.ə.ti taɪm/", vi: "Thời gian chất lượng" },
        { en: "Hang out with friends", pos: "(v phrase)", ipa: "/hæŋ aʊt wɪð frendz/", vi: "Đi chơi với bạn" },
        { en: "Catch up with friends", pos: "(v phrase)", ipa: "/kætʃ ʌp wɪð frendz/", vi: "Gặp gỡ, hỏi thăm bạn bè" },
        { en: "Go for a stroll", pos: "(v phrase)", ipa: "/ɡəʊ fɔːr ə strəʊl/", vi: "Đi dạo" },
        { en: "Eat out / Dine out", pos: "(v phrase)", ipa: "/iːt aʊt/", vi: "Ăn ở nhà hàng" },
        { en: "Escape the city", pos: "(v phrase)", ipa: "/ɪˈskeɪp ðə ˈsɪt.i/", vi: "Trốn khỏi thành phố" },
        { en: "Pursue my hobbies", pos: "(v phrase)", ipa: "/pəˈsjuː maɪ ˈhɒb.iz/", vi: "Theo đuổi sở thích" },
        { en: "Do some window shopping", pos: "(v phrase)", ipa: "/duː sʌm ˈwɪn.dəʊ ˌʃɒp.ɪŋ/", vi: "Đi ngắm đồ nhưng không mua" },
        { en: "Lazy Sunday", pos: "(n phrase)", ipa: "/ˈleɪ.zi ˈsʌn.deɪ/", vi: "Ngày chủ nhật lười biếng" },
        { en: "Night owl", pos: "(n phrase)", ipa: "/naɪt aʊl/", vi: "Cú đêm" },
        { en: "Heavy sleeper", pos: "(n phrase)", ipa: "/ˈhev.i ˈsliː.pər/", vi: "Người ngủ say" },
        { en: "Light sleeper", pos: "(n phrase)", ipa: "/laɪt ˈsliː.pər/", vi: "Người ngủ thính" },
        { en: "Sound sleep", pos: "(n phrase)", ipa: "/saʊnd sliːp/", vi: "Giấc ngủ ngon/sâu" },
        { en: "Sleep like a log", pos: "(idiom)", ipa: "/sliːp laɪk ə lɒɡ/", vi: "Ngủ say như chết" },
        { en: "Toss and turn", pos: "(v phrase)", ipa: "/tɒs ənd tɜːn/", vi: "Trằn trọc" },
        { en: "Suffer from insomnia", pos: "(v phrase)", ipa: "/ˈsʌf.ər frɒm ɪnˈsɒm.ni.ə/", vi: "Bị mất ngủ" },
        { en: "Have a nightmare", pos: "(v phrase)", ipa: "/hæv ə ˈnaɪt.meər/", vi: "Gặp ác mộng" },
        { en: "Wake up refreshed", pos: "(v phrase)", ipa: "/weɪk ʌp rɪˈfreʃt/", vi: "Tỉnh dậy thấy sảng khoái" },
        { en: "Feel groggy", pos: "(v phrase)", ipa: "/fiːl ˈɡrɒɡ.i/", vi: "Cảm thấy lờ đờ" },
        { en: "Take a power nap", pos: "(v phrase)", ipa: "/teɪk ə ˈpaʊ.ə næp/", vi: "Chợp mắt nhanh" },
        { en: "Fall asleep", pos: "(v phrase)", ipa: "/fɔːl əˈsliːp/", vi: "Chìm vào giấc ngủ" },
        { en: "Set an alarm", pos: "(v phrase)", ipa: "/set ən əˈlɑːm/", vi: "Đặt báo thức" },
        { en: "Lack of sleep", pos: "(n phrase)", ipa: "/læk əv sliːp/", vi: "Thiếu ngủ" },
        { en: "Improve sleep quality", pos: "(v phrase)", ipa: "/ɪmˈpruːv sliːp ˈkwɒl.ə.ti/", vi: "Cải thiện chất lượng giấc ngủ" },
        { en: "Keep fit / Stay in shape", pos: "(v phrase)", ipa: "/kiːp fɪt/", vi: "Giữ dáng" },
        { en: "Lead a sedentary lifestyle", pos: "(v phrase)", ipa: "/liːd ə ˈsed.ən.tər.i ˈlaɪf.staɪl/", vi: "Lối sống thụ động" },
        { en: "Hit the gym", pos: "(v phrase)", ipa: "/hɪt ðə dʒɪm/", vi: "Đi tập gym" },
        { en: "Do yoga / Do aerobics", pos: "(v phrase)", ipa: "/duː ˈjəʊ.ɡə/", vi: "Tập yoga / nhịp điệu" },
        { en: "Go for a jog", pos: "(v phrase)", ipa: "/ɡəʊ fɔːr ə dʒɒɡ/", vi: "Đi chạy bộ" },
        { en: "Work out", pos: "(v phrase)", ipa: "/wɜːk aʊt/", vi: "Tập luyện thể dục" },
        { en: "Burn calories", pos: "(v phrase)", ipa: "/bɜːn ˈkæl.ər.iz/", vi: "Đốt calo" },
        { en: "Boost my mood", pos: "(v phrase)", ipa: "/buːst maɪ muːd/", vi: "Cải thiện tâm trạng" },
        { en: "Relieve stress", pos: "(v phrase)", ipa: "/rɪˈliːv stres/", vi: "Giảm căng thẳng" },
        { en: "Strengthen immune system", pos: "(v phrase)", ipa: "/ˈstreŋ.θən ɪˈmjuːn ˈsɪs.təm/", vi: "Tăng cường hệ miễn dịch" },
        { en: "Build muscle", pos: "(v phrase)", ipa: "/bɪld ˈmʌs.əl/", vi: "Xây dựng cơ bắp" },
        { en: "Physical health", pos: "(n phrase)", ipa: "/ˈfɪz.ɪ.kəl helθ/", vi: "Sức khỏe thể chất" },
        { en: "Mental health", pos: "(n phrase)", ipa: "/ˈmen.təl helθ/", vi: "Sức khỏe tinh thần" },
        { en: "Brisk walking", pos: "(n phrase)", ipa: "/brɪsk ˈwɔː.kɪŋ/", vi: "Đi bộ nhanh" },
        { en: "Outdoor activities", pos: "(n phrase)", ipa: "/ˈaʊt.dɔːr ækˈtɪv.ə.tiz/", vi: "Các hoạt động ngoài trời" },
        { en: "Private vehicle", pos: "(n phrase)", ipa: "/ˈpraɪ.vət ˈviː.ɪ.kəl/", vi: "Phương tiện cá nhân" },
        { en: "Public transport", pos: "(n phrase)", ipa: "/ˈpʌb.lɪk ˈtræn.spɔːt/", vi: "Phương tiện công cộng" },
        { en: "Daily commuter", pos: "(n phrase)", ipa: "/ˈdeɪ.li kəˈmjuː.tər/", vi: "Người đi làm/học hàng ngày" },
        { en: "Get around", pos: "(phrasal v)", ipa: "/ɡet əˈraʊnd/", vi: "Đi lại quanh thành phố" },
        { en: "Stuck in traffic", pos: "(adj phrase)", ipa: "/stʌk ɪn ˈtræf.ɪk/", vi: "Tắc đường" },
        { en: "Rush hour / Peak hour", pos: "(n phrase)", ipa: "/rʌʃ ˈaʊər/", vi: "Giờ cao điểm" },
        { en: "Packed like sardines", pos: "(idiom)", ipa: "/pækt laɪk sɑːˈdiːnz/", vi: "Đông nghẹt (như cá mòi)" },
        { en: "Catch the bus", pos: "(v phrase)", ipa: "/kætʃ ðə bʌs/", vi: "Bắt xe buýt" },
        { en: "Miss the bus", pos: "(v phrase)", ipa: "/mɪs ðə bʌs/", vi: "Lỡ xe buýt" },
        { en: "Environmentally friendly", pos: "(adj)", ipa: "/ɪnˌvaɪ.rənˈmen.təl.i ˈfrend.li/", vi: "Thân thiện với môi trường" },
        { en: "Cost-effective", pos: "(adj)", ipa: "/kɒst ɪˈfek.tɪv/", vi: "Tiết kiệm chi phí" },
        { en: "Flexible", pos: "(adj)", ipa: "/ˈflek.sə.bəl/", vi: "Linh hoạt" },
        { en: "Find a parking space", pos: "(v phrase)", ipa: "/faɪnd ə ˈpɑː.kɪŋ speɪs/", vi: "Tìm chỗ đậu xe" },
        { en: "Rely on", pos: "(v phrase)", ipa: "/rɪˈlaɪ ɒn/", vi: "Phụ thuộc vào" },
        { en: "Air pollution", pos: "(n phrase)", ipa: "/eər pəˈluː.ʃən/", vi: "Ô nhiễm không khí" },
        { en: "Exhaust fumes", pos: "(n phrase)", ipa: "/ɪɡˈzɔːst fjuːmz/", vi: "Khói thải từ xe cộ" },
        { en: "Convenient way to travel", pos: "(n phrase)", ipa: "/kənˈviː.ni.ənt weɪ tu ˈtræv.əl/", vi: "Cách di chuyển thuận tiện" },
        { en: "Ride a motorbike", pos: "(v phrase)", ipa: "/raɪd ə ˈməʊ.tə.baɪk/", vi: "Lái xe máy" },
        { en: "Book a Grab/taxi", pos: "(v phrase)", ipa: "/bʊk ə ɡræb/", vi: "Đặt xe công nghệ/taxi" },
        { en: "It depends on", pos: "(v phrase)", ipa: "/ɪt dɪˈpendz ɒn/", vi: "Nó còn tùy vào" },
        { en: "As much as possible", pos: "(phrase)", ipa: "/æz mʌtʃ æz ˈpɒs.ə.bəl/", vi: "Nhiều nhất có thể" },
        { en: "Work around the clock", pos: "(idiom)", ipa: "/wɜːk əˈraʊnd ðə klɒk/", vi: "Làm việc/học tập suốt ngày đêm" },
        { en: "Do wonders for", pos: "(idiom)", ipa: "/duː ˈwʌn.dəz fɔːr/", vi: "Có lợi ích tuyệt vời/kỳ diệu cho..." },
        { en: "Every other day", pos: "(adv. phrase)", ipa: "/ˈev.ri ˈʌð.ər deɪ/", vi: "Cách một ngày (2 ngày 1 lần)" },
        { en: "A creature of habit", pos: "(idiom)", ipa: "/ə ˈkriː.tʃər əv ˈhæb.ɪt/", vi: "Người sống theo thói quen" },
        { en: "Burn the candle at both ends", pos: "(idiom)", ipa: "/bɜːn ðə ˈkæn.dəl æt bəʊθ endz/", vi: "Vắt kiệt sức lực (thức khuya dậy sớm)" },
        { en: "Hit the sack", pos: "(idiom)", ipa: "/hɪt ðə sæk/", vi: "Đi ngủ" }
    ];

    let vocabularyList = initialVocabulary.map(item => ({...item, status: 'new'}));
    
    let currentIndex = 0;
    let isRevealed = false;
    let availableVoices = [];
    
    // Global settings for audio
    let selectedVoiceIndex = -1; // -1 means auto-detect
    let readingRate = 0.8; // Default slow speed

    // Elements
    const elements = {
        vnText: document.getElementById('vn-text'),
        enText: document.getElementById('en-text'),
        ipaText: document.getElementById('ipa-text'), 
        posText: document.getElementById('pos-text'),
        exText: document.getElementById('example-text'),
        answerArea: document.getElementById('answer-area'),
        btnReveal: document.getElementById('btn-reveal'),
        reviewActions: document.getElementById('review-actions'),
        statusMsg: document.getElementById('status-msg'),
        progress: document.getElementById('progress'),
        currentStatus: document.getElementById('current-status'),
        listModal: document.getElementById('list-modal'),
        listContent: document.getElementById('vocab-list-content'),
        statsModal: document.getElementById('stats-modal'),
        statLearned: document.getElementById('stat-learned'),
        statLearning: document.getElementById('stat-learning'),
        statNew: document.getElementById('stat-new'),
        recommendList: document.getElementById('recommend-list'),
        settingsModal: document.getElementById('settings-modal'),
        voiceSelect: document.getElementById('voice-select'),
        speedRange: document.getElementById('speed-range'),
        speedDisplay: document.getElementById('speed-display')
    };

    // === SETUP AUDIO (PURE SYSTEM SPEECH) ===
    function loadVoices() {
        availableVoices = window.speechSynthesis.getVoices();
        
        elements.voiceSelect.innerHTML = '';
        
        const defaultOption = document.createElement('option');
        defaultOption.value = -1;
        defaultOption.text = "Tự động chọn (Tốt nhất)";
        elements.voiceSelect.appendChild(defaultOption);

        availableVoices.forEach((voice, index) => {
            if(voice.lang.includes('en')) {
                const option = document.createElement('option');
                option.value = index;
                option.text = `${voice.name} (${voice.lang})`;
                if (index === selectedVoiceIndex) option.selected = true;
                elements.voiceSelect.appendChild(option);
            }
        });
    }
    
    if (speechSynthesis.onvoiceschanged !== undefined) {
        speechSynthesis.onvoiceschanged = loadVoices;
    }
    setTimeout(loadVoices, 100);

    function playAudio(text) {
        window.speechSynthesis.cancel();
        const utterance = new SpeechSynthesisUtterance(text);
        
        if (selectedVoiceIndex !== -1 && availableVoices[selectedVoiceIndex]) {
            utterance.voice = availableVoices[selectedVoiceIndex];
        } else {
            let preferredVoice = availableVoices.find(voice => 
                (voice.name.includes('Google') && voice.lang.includes('en')) || 
                (voice.name.includes('Premium') && voice.lang.includes('en')) ||
                (voice.name.includes('Samantha') && voice.lang.includes('en'))
            );

            if (!preferredVoice) {
                preferredVoice = availableVoices.find(voice => voice.lang === 'en-GB' || voice.lang === 'en_GB');
            }
            if (!preferredVoice) {
                preferredVoice = availableVoices.find(voice => voice.lang.includes('en'));
            }

            if (preferredVoice) utterance.voice = preferredVoice;
        }
        
        utterance.rate = readingRate; 
        utterance.pitch = 1.0;
        utterance.volume = 1.0;

        utterance.onerror = (e) => console.log('Speech error:', e);
        window.speechSynthesis.speak(utterance);
    }

    // --- SETTINGS FUNCTIONS ---
    function toggleSettings() {
        const isHidden = elements.settingsModal.style.display === 'none' || elements.settingsModal.style.display === '';
        if (isHidden) {
            elements.settingsModal.style.display = 'flex';
            if(availableVoices.length === 0) loadVoices();
        } else {
            elements.settingsModal.style.display = 'none';
        }
    }

    function updateVoiceSettings() {
        selectedVoiceIndex = parseInt(elements.voiceSelect.value);
    }

    function updateSpeedSettings() {
        readingRate = parseFloat(elements.speedRange.value);
        elements.speedDisplay.innerText = readingRate;
    }
    
    function testVoice() {
        playAudio("Hello, this is a test for English voice.");
    }

    // --- OTHER LOGIC ---
    function shuffleVocabulary() {
        for (let i = vocabularyList.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [vocabularyList[i], vocabularyList[j]] = [vocabularyList[j], vocabularyList[i]];
        }
        currentIndex = 0;
        loadCard(0);
        elements.statusMsg.innerText = "🔀 Đã đảo thứ tự từ vựng!";
        setTimeout(() => elements.statusMsg.innerText = "", 2000);
    }

    function loadCard(index) {
        if (index < 0) currentIndex = vocabularyList.length - 1;
        else if (index >= vocabularyList.length) currentIndex = 0;
        else currentIndex = index;

        const item = vocabularyList[currentIndex];

        elements.vnText.innerText = item.vi;
        elements.enText.innerText = item.en;
        elements.posText.innerText = item.pos;
        
        if (elements.exText) {
             if(item.ex) {
                elements.exText.innerText = `Ví dụ: "${item.ex}"`;
                elements.exText.style.display = 'block';
            } else {
                elements.exText.style.display = 'none';
            }
        }
        
        if (item.ipa) {
            elements.ipaText.innerText = item.ipa;
            elements.ipaText.style.display = 'block';
        } else {
            elements.ipaText.style.display = 'none';
        }
        
        elements.answerArea.style.display = 'none';
        elements.reviewActions.style.display = 'none';
        elements.btnReveal.style.display = 'block';
        elements.btnReveal.disabled = false;
        elements.btnReveal.innerText = "XEM ĐÁP ÁN";
        elements.statusMsg.innerText = "";
        
        elements.progress.innerText = `CÂU ${currentIndex + 1} / ${vocabularyList.length}`;
        updateStatusBadge(item.status);
        
        isRevealed = false;
    }

    function updateStatusBadge(status) {
        elements.currentStatus.className = 'status-badge';
        if (status === 'learned') {
            elements.currentStatus.innerText = "Đã thuộc";
            elements.currentStatus.classList.add('status-learned');
        } else if (status === 'learning') {
            elements.currentStatus.innerText = "Chưa thuộc";
            elements.currentStatus.classList.add('status-learning');
        } else {
            elements.currentStatus.innerText = "Mới";
            elements.currentStatus.classList.add('status-new');
        }
    }

    function revealAnswer() {
        isRevealed = true;
        elements.btnReveal.disabled = true;
        elements.answerArea.style.display = 'block';
        playAudio(vocabularyList[currentIndex].en);
        elements.btnReveal.style.display = 'none'; 
        elements.reviewActions.style.display = 'flex'; 
    }

    function playCurrentAudio() {
        playAudio(vocabularyList[currentIndex].en);
    }

    function markStatus(status) {
        vocabularyList[currentIndex].status = status;
        
        // Save progress to local storage with specific key
        const progress = JSON.parse(localStorage.getItem('vocab_progress_daily_life') || '{}');
        progress[currentIndex] = status;
        localStorage.setItem('vocab_progress_daily_life', JSON.stringify(progress));

        updateStatusBadge(status);
        setTimeout(() => { changeCard(1); }, 300);
    }

    function loadProgress() {
        const progress = JSON.parse(localStorage.getItem('vocab_progress_daily_life') || '{}');
        vocabularyList.forEach((item, index) => {
            if (progress[index]) {
                item.status = progress[index];
            }
        });
    }

    function changeCard(step) {
        loadCard(currentIndex + step);
    }

    function toggleList() {
        const isHidden = elements.listModal.style.display === 'none' || elements.listModal.style.display === '';
        if (isHidden) {
            renderList();
            elements.listModal.style.display = 'flex';
        } else {
            elements.listModal.style.display = 'none';
        }
    }

    function renderList() {
        elements.listContent.innerHTML = '';
        vocabularyList.forEach((item, index) => {
            const div = document.createElement('div');
            div.className = `list-item ${index === currentIndex ? 'active' : ''}`;
            let statusIcon = '⚪';
            if (item.status === 'learned') statusIcon = '✅';
            if (item.status === 'learning') statusIcon = '🔸';
            div.innerHTML = `<div style="display:flex; align-items:center;"><span style="margin-right:8px; font-size: 12px;">${statusIcon}</span><strong>${item.en}</strong></div><div style="font-size:12px; color:#666;">${index + 1}</div>`;
            div.onclick = () => { currentIndex = index; loadCard(currentIndex); toggleList(); };
            elements.listContent.appendChild(div);
        });
    }

    function toggleStats() {
        const isHidden = elements.statsModal.style.display === 'none' || elements.statsModal.style.display === '';
        if (isHidden) { renderStats(); elements.statsModal.style.display = 'flex'; } else { elements.statsModal.style.display = 'none'; }
    }

    function renderStats() {
        const learnedCount = vocabularyList.filter(i => i.status === 'learned').length;
        const learningCount = vocabularyList.filter(i => i.status === 'learning').length;
        const newCount = vocabularyList.filter(i => i.status === 'new').length;
        elements.statLearned.innerText = learnedCount;
        elements.statLearning.innerText = learningCount;
        elements.statNew.innerText = newCount;
        let recommendItems = vocabularyList.map((item, index) => ({ ...item, originalIndex: index })).filter(i => i.status === 'learning');
        elements.recommendList.innerHTML = '';
        if (recommendItems.length === 0) {
            const newItems = vocabularyList.map((item, index) => ({ ...item, originalIndex: index })).filter(i => i.status === 'new').slice(0, 5);
            if (newItems.length > 0) {
                elements.recommendList.innerHTML = '<div style="color:#777; font-style:italic; padding:10px;">Bạn đã thuộc hết các từ cần ôn. Hãy học từ mới:</div>';
                newItems.forEach(item => createRecommendItem(item));
            } else {
                elements.recommendList.innerHTML = '<div style="color:green; padding:10px; text-align:center;">🎉 Tuyệt vời! Bạn đã thuộc hết toàn bộ danh sách.</div>';
            }
        } else {
            recommendItems.forEach(item => createRecommendItem(item));
        }
    }

    function createRecommendItem(item) {
        const div = document.createElement('div');
        div.className = 'recommend-item';
        div.innerHTML = `🔸 <strong>${item.en}</strong> <span style="font-size:12px; color:#999;">(${item.vi})</span>`;
        div.onclick = () => { currentIndex = item.originalIndex; loadCard(currentIndex); toggleStats(); };
        elements.recommendList.appendChild(div);
    }

    loadProgress();
    loadCard(0);
</script>

</body>
</html>
