<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hệ Thống Theo Dõi Người Liên Kết v13.3</title>
    <style>
        :root {
            --card-bg: rgba(255, 255, 255, 0.85);
            --text-main: #1e293b;
            --text-sub: #64748b;
            --border-color: rgba(255, 255, 255, 0.9);
            --good: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --info: #3b82f6;
            --love: #a855f7;
            --money: #059669;
        }

        body {
            font-family: '-apple-system', BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, #e2f1ff 0%, #f5ebff 50%, #fff5dc 100%);
            background-size: 300% 300%;
            animation: auraAnimation 14s ease infinite;
            color: var(--text-main);
            margin: 0;
            padding: 20px 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
            box-sizing: border-box;
        }

        @keyframes auraAnimation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        #particles-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .app-container {
            width: 100%;
            max-width: 850px;
            position: relative;
            z-index: 2;
        }

        .page {
            display: none;
            background: var(--card-bg);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.6);
            border-radius: 32px;
            box-shadow: 0 30px 60px -15px rgba(15, 23, 42, 0.08), inset 0 2px 4px rgba(255,255,255,0.5);
            padding: 35px 30px;
            box-sizing: border-box;
            animation: fadeIn 0.4s ease-out forwards;
        }

        .page.active { display: block; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 { 
            text-align: center; 
            margin: 0 0 8px 0; 
            font-size: 30px; 
            font-weight: 800; 
            letter-spacing: -0.5px;
            background: linear-gradient(to right, #1e40af, #6d28d9);
            /* standard property for compatibility */
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .subtitle { text-align: center; color: var(--text-sub); font-size: 11px; margin-bottom: 30px; font-weight: 700; text-transform: uppercase; letter-spacing: 2px; }

        .back-btn {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: rgba(255, 255, 255, 0.7);
            border: 1px solid rgba(0, 0, 0, 0.05);
            padding: 8px 16px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 700;
            color: #1e40af;
            cursor: pointer;
            transition: all 0.2s;
            margin-bottom: 20px;
        }
        .back-btn:hover { background: #fff; transform: translateX(-3px); box-shadow: 0 4px 10px rgba(0,0,0,0.05); }

        /* ==================== MỤC LỤC ĐIỀU HƯỚNG ==================== */
        .home-menu-trigger { display: flex; justify-content: center; margin: 40px 0; }
        .btn-toggle-menu {
            background: linear-gradient(135deg, #2563eb 0%, #7c3aed 100%); color: white; border: none;
            padding: 16px 40px; font-size: 16px; font-weight: 700; border-radius: 50px; cursor: pointer;
            box-shadow: 0 10px 25px rgba(124, 58, 237, 0.3); transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: flex; align-items: center; gap: 10px;
        }
        .btn-toggle-menu:hover { transform: scale(1.05); box-shadow: 0 15px 30px rgba(124, 58, 237, 0.45); }

        /* Chuyển đổi linh hoạt hiển thị Grid menu */
        .menu-grid { display: none; grid-template-columns: repeat(2, 1fr); gap: 20px; animation: slideDown 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards; }
        @media (max-width: 600px) { .menu-grid.open { grid-template-columns: 1fr; } }
        .menu-grid.open { display: grid; }

        @keyframes slideDown { from { opacity: 0; transform: translateY(-20px); } to { opacity: 1; transform: translateY(0); } }

        .menu-item {
            background: rgba(255, 255, 255, 0.6); border: 1px solid rgba(255, 255, 255, 0.8); border-radius: 24px;
            padding: 24px; cursor: pointer; transition: all 0.25s ease; display: flex; flex-direction: column; gap: 8px;
        }
        .menu-item:hover { transform: translateY(-5px); background: white; box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.05); }
        .menu-item .icon { font-size: 32px; }
        .menu-item .title { font-size: 16px; font-weight: 700; color: #0f172a; }
        .menu-item .desc { font-size: 12px; color: var(--text-sub); line-height: 1.4; }

        .m-eat:hover { border-color: var(--info); }
        .m-mood:hover { border-color: var(--love); }
        .m-health:hover { border-color: var(--danger); }
        .m-act:hover { border-color: var(--warning); }
        .m-money:hover { border-color: var(--money); }
        .m-letter:hover { border-color: #f43f5e; }

        /* ==================== ĐỊNH LƯỢNG TIẾN TRÌNH % ĐỘC LẬP ==================== */
        .energy-time-container { margin-bottom: 25px; }
        .energy-block-item, .hydration-block-item { display: none; animation: fadeIn 0.35s ease forwards; }
        .energy-block-item.show-block, .hydration-block-item.show-block { display: block; }

        .stat-bar-container { background: #e2e8f0; height: 10px; border-radius: 10px; overflow: hidden; margin: 8px 0; position: relative; }
        .stat-bar-fill { height: 100%; width: 50%; transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1); }
        .fill-sang { background: linear-gradient(90deg, #ff7e5f, #feb47b); }
        .fill-trua { background: linear-gradient(90deg, #10b981, #059669); }
        .fill-chieu { background: linear-gradient(90deg, #ec4899, #a855f7); }
        .fill-toi { background: linear-gradient(90deg, #1e3a8a, #3b82f6); }
        .fill-drink { background: linear-gradient(90deg, #06b6d4, #3b82f6); }
        
        .eat-btn-group { display: grid; grid-template-columns: repeat(3, 1fr); gap: 6px; margin-top: 8px; }
        .eat-status-btn { background: white; border: 1px solid #e2e8f0; padding: 8px 4px; border-radius: 10px; font-size: 11px; font-weight: 700; cursor: pointer; transition: all 0.2s; color: #475569; text-align: center;}
        .eat-status-btn.active-good { background: #d1fae5; color: #065f46; border-color: #10b981; }
        .eat-status-btn.active-warn { background: #fef3c7; color: #92400e; border-color: #f59e0b; }
        .eat-status-btn.active-danger { background: #fee2e2; color: #991b1b; border-color: #ef4444; }

        .time-filter-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; margin: 12px 0 25px 0; }
        .time-btn { background: white; border: 1px solid #cbd5e1; padding: 12px 6px; border-radius: 14px; font-size: 12px; font-weight: 700; cursor: pointer; text-align: center; color: #475569; transition: all 0.2s ease; display: flex; flex-direction: column; align-items: center; gap: 4px;}
        .time-btn.active { background: linear-gradient(135deg, #0f172a 0%, #334155 100%); color: white; border-color: #0f172a; box-shadow: 0 4px 12px rgba(15, 23, 42, 0.15); }

        /* ==================== ĐỊNH DẠNG NÚT GẠT SWITCH SỨC KHỎE ==================== */
        .switch { position: relative; display: inline-block; width: 44px; height: 24px; flex-shrink: 0; }
        .switch input { opacity: 0; width: 0; height: 0; }
        .slider-legacy {
            position: absolute; cursor: pointer; top: 0; left: 0; right: 0; bottom: 0;
            background-color: #cbd5e1; transition: .3s; border-radius: 24px;
        }
        .slider-legacy:before {
            position: absolute; content: ""; height: 18px; width: 18px; left: 3px; bottom: 3px;
            background-color: white; transition: .3s; border-radius: 50%; box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        input:checked + .slider-legacy { background-color: #ef4444; }
        input:checked + .slider-legacy:before { transform: translateX(20px); }

        .health-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px; margin-top: 15px; }
        @media (max-width: 768px) { .health-grid { grid-template-columns: 1fr; } }

        .health-help-link {
            font-size: 11px; color: var(--danger); text-decoration: none; font-weight: 700;
            background: #fef2f2; padding: 4px 10px; border-radius: 8px; border: 1px solid #fca5a5;
            transition: all 0.2s; cursor: pointer; display: inline-block;
        }
        .health-help-link:hover { background: #fee2e2; transform: scale(1.05); }

        /* Khối SOS */
        .sos-alert-box {
            background: linear-gradient(135deg, #fee2e2 0%, #fff1f2 100%);
            border: 2px dashed var(--danger); border-radius: 20px; padding: 20px;
            text-align: center; margin-bottom: 25px;
        }
        .btn-sos-trigger {
            background: linear-gradient(135deg, #dc2626 0%, #ef4444 100%);
            color: white; border: none; padding: 12px 30px; border-radius: 50px;
            font-size: 15px; font-weight: 800; cursor: pointer; box-shadow: 0 6px 15px rgba(220, 38, 38, 0.3);
            transition: all 0.3s;
        }
        .btn-sos-trigger:hover { transform: scale(1.05); box-shadow: 0 10px 20px rgba(220, 38, 38, 0.5); }
        .btn-sos-trigger.activating { animation: pulseRed 0.8s infinite linear; }

        .period-link-btn { 
            display: flex; align-items: center; justify-content: space-between; 
            background: #fff1f2; padding: 14px 14px; border-radius: 12px; 
            border: 1px solid #fda4af; color: #e11d48; font-size: 13px; 
            text-decoration: none; font-weight: 700; margin-top: 10px; 
            transition: all 0.2s; cursor: pointer;
        }
        .period-link-btn:hover { background: #ffe4e6; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(225, 29, 72, 0.1); }

        /* Giao diện sổ hướng dẫn cứu trợ (Modal Popup) */
        .health-modal {
            display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(15, 23, 42, 0.6); backdrop-filter: blur(8px);
            z-index: 999; justify-content: center; align-items: center; padding: 20px; box-sizing: border-box;
        }
        .modal-content {
            background: white; width: 100%; max-width: 500px; border-radius: 28px;
            padding: 30px; box-sizing: border-box; animation: slideUp 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25);
        }
        @keyframes slideUp { from { transform: translateY(30px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        .modal-header { font-size: 18px; font-weight: 800; color: #991b1b; margin-bottom: 15px; display: flex; align-items: center; gap: 8px; }
        .modal-body { font-size: 13px; line-height: 1.6; color: #334155; margin-bottom: 20px; max-height: 300px; overflow-y: auto; background: #f8fafc; padding: 15px; border-radius: 14px; }
        .btn-close-modal { width: 100%; padding: 12px; background: #64748b; color: white; border: none; border-radius: 12px; font-weight: 700; cursor: pointer; }

        /* ==================== MỤC TÂM TRẠNG NÂNG CAO ==================== */
        .mood-box-select { width: 100%; padding: 12px; border-radius: 14px; border: 1px solid rgba(226, 232, 240, 0.9); font-size: 14px; background: white; margin-bottom: 20px; outline: none; font-weight: 600; }
        .btn-action-save { width: 100%; padding: 15px; border-radius: 16px; border: none; background: linear-gradient(135deg, #a855f7 0%, #7c3aed 100%); color: white; font-size: 14px; font-weight: 700; cursor: pointer; box-shadow: 0 8px 20px rgba(124, 58, 237, 0.25); }

        /* ==================== MỤC VÍ QUỸ CHUNG ==================== */
        .wallet-card { background: linear-gradient(135deg, #059669 0%, #10b981 100%); color: white; border-radius: 20px; padding: 25px; margin-bottom: 20px; box-shadow: 0 10px 20px rgba(5, 150, 105, 0.2); }
        .wallet-balance { font-size: 28px; font-weight: 800; margin: 8px 0; letter-spacing: -0.5px; }
        .ledger-box { background: white; border-radius: 16px; border: 1px solid #e2e8f0; padding: 15px; }

        /* LAYOUT CHUNG */
        .page-eat { background: linear-gradient(to bottom right, rgba(239, 246, 255, 0.9), rgba(255, 255, 255, 0.75)); }
        .page-mood { background: linear-gradient(to bottom right, rgba(250, 245, 255, 0.9), rgba(255, 255, 255, 0.75)); }
        .page-health { background: linear-gradient(to bottom right, rgba(254, 242, 242, 0.9), rgba(255, 255, 255, 0.75)); }
        .page-act { background: linear-gradient(to bottom right, rgba(254, 252, 232, 0.9), rgba(255, 255, 255, 0.75)); }
        .page-money { background: linear-gradient(to bottom right, rgba(209, 250, 229, 0.9), rgba(255, 255, 255, 0.75)); }
        .page-letter { background: linear-gradient(to bottom right, rgba(255, 241, 242, 0.9), rgba(255, 255, 255, 0.75)); }

        .section-title { font-size: 16px; font-weight: 700; margin-bottom: 16px; color: #0f172a; display: flex; align-items: center; gap: 10px; }
        .section-title::before { content: ''; display: inline-block; width: 6px; height: 16px; border-radius: 10px; background: var(--info); }
        .love-title::before { background: var(--love); }
        .health-title::before { background: var(--danger); }
        .money-title::before { background: var(--money); }
        .letter-title::before { background: var(--warning); }

        .status-card { background: rgba(255,255,255,0.9); border: 1px solid var(--border-color); border-radius: 18px; padding: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.01); }
        .card-sub-title { font-size: 11px; font-weight: 700; color: var(--text-sub); margin-bottom: 10px; text-transform: uppercase; letter-spacing: 0.5px; }

        .menu-tabs { display: grid; grid-template-columns: repeat(3, 1fr); gap: 6px; margin-bottom: 10px; }
        .tab-btn { background: rgba(241, 245, 249, 0.8); border: none; padding: 10px; font-size: 11px; font-weight: 700; border-radius: 10px; cursor: pointer; color: #475569; }
        .tab-btn.active { background: #1e40af; color: white; }
        
        .scroll-box { background: rgba(255,255,255,0.95); border: 1px solid var(--border-color); border-radius: 18px; padding: 14px; max-height: 320px; overflow-y: auto; }
        .menu-grid-items { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 8px; }

        .item-list { display: flex; flex-direction: column; gap: 8px; }
        .row-item {
            display: flex; align-items: center; justify-content: space-between; gap: 10px;
            background: white; padding: 12px 14px; border-radius: 12px;
            border: 1px solid rgba(241, 245, 249, 0.9); font-size: 13px;
        }
        .row-item.hidden { display: none !important; }

        .letter-link-btn { display: flex; align-items: center; justify-content: center; gap: 10px; background: linear-gradient(135deg, #1e40af 0%, #3b82f6 100%); color: white; padding: 16px; border-radius: 14px; text-decoration: none; font-weight: 700; box-shadow: 0 4px 14px rgba(59, 130, 246, 0.25); }

        .activity-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 8px; }
        .mood-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(130px, 1fr)); gap: 12px; }
        .mood-btn {
            background: white; border: 1px solid rgba(226, 232, 240, 0.8); padding: 16px 10px; border-radius: 16px;
            cursor: pointer; font-weight: 600; font-size: 13px; text-align: center; display: flex;
            flex-direction: column; align-items: center; gap: 8px; transition: all 0.25s ease;
        }
        .mood-btn.active { color: white; font-weight: 700; scale: 1.04; }

        .custom-cb { width: 18px; height: 18px; accent-color: var(--love); cursor: pointer; }
        .footer-status { text-align: center; font-size: 11px; color: #94a3b8; margin-top: 25px; font-weight: 500; }
    </style>
</head>
<body>

<canvas id="particles-canvas"></canvas>

<!-- TỔNG ĐÀI CỨU TRỢ POPUP -->
<div id="emergency-modal" class="health-modal">
    <div class="modal-content">
        <div class="modal-header" id="modal-title-target">🚑 Cẩm Nang Sơ Cứu Khẩn Cấp</div>
        <div class="modal-body" id="modal-body-target">Nội dung hướng dẫn y tế...</div>
        <button class="btn-close-modal" onclick="closeEmergencyModal()">Đã hiểu, đóng cẩm nang</button>
    </div>
</div>

<div class="app-container">

    <!-- ==================== 1. TRANG CHỦ & MỤC LỤC ==================== -->
    <div id="page-home" class="page active">
        <h1>HỆ THỐNG THEO DÕI LIÊN KẾT</h1>
        <div class="subtitle">Bản thiết kế Hệ thống phân mục Aura v13.3</div>
        
        <div class="home-menu-trigger">
            <button class="btn-toggle-menu" onclick="toggleMenuGrid()">
                <span>📋 Mở Mục Lục Điều Hướng</span>
                <span id="menu-arrow">▼</span>
            </button>
        </div>

        <div id="main-menu-grid" class="menu-grid">
            <div class="menu-item m-eat" onclick="navigateTo('page-eat')">
                <span class="icon">🍽️</span>
                <span class="title">Ăn Uống & Cấp Ẩm</span>
                <span class="desc">Bảng định lượng năng lượng và cấp ẩm đồng bộ, tách biệt 4 buổi sáng-trưa-chiều-tối riêng biệt.</span>
            </div>
            <div class="menu-item m-mood" onclick="navigateTo('page-mood')">
                <span class="icon">🧠</span>
                <span class="title">Tình Trạng Tâm Trạng</span>
                <span class="desc">Hệ thống phân tích nguyên nhân, định vị mức độ khẩn cấp và đề xuất giải pháp Aura thông minh.</span>
            </div>
            <div class="menu-item m-health" onclick="navigateTo('page-health')">
                <span class="icon">🏥</span>
                <span class="title">Sức Khỏe & Cứu Thương</span>
                <span class="desc">Khắc phục lỗi công tắc gạt. Liên kết mượt mà đến trang nhật ký chu kỳ độc lập.</span>
            </div>
            <div class="menu-item m-act" onclick="navigateTo('page-act')">
                <span class="icon">💖</span>
                <span class="title">Hoạt Động Hẹn Hò</span>
                <span class="desc">Khám phá danh mục đầy đủ 50 điều mong muốn trải nghiệm cùng nhau.</span>
            </div>
            <!-- ĐÃ BỔ SUNG: Khối Menu Quỹ Hẹn Hò -->
            <div class="menu-item m-money" onclick="navigateTo('page-money')">
                <span class="icon">💵</span>
                <span class="title">Ví Tài Chính & Quỹ Chung</span>
                <span class="desc">Theo dõi số dư quỹ hẹn hò, ghi chép nhanh tình phí và lịch sử đóng góp thu chi của cả hai.</span>
            </div>
            <div class="menu-item m-letter" onclick="navigateTo('page-letter')">
                <span class="icon">💌</span>
                <span class="title">Hòm Thư Góp Ý</span>
                <span class="desc">Ghi lại tâm thư, nhận xét khách quan và đóng góp ý kiến xây dựng.</span>
            </div>
        </div>

        <div class="footer-status" style="margin-top: 50px;">Hệ thống vận hành an toàn • <span class="clock-display">--:--:--</span></div>
    </div>


    <!-- ==================== 2. TRANG CON: ĂN UỐNG & CẤP ẨM ==================== -->
    <div id="page-eat" class="page page-eat">
        <button class="back-btn" onclick="navigateTo('page-home')">⬅️ Quay lại Trang Chủ</button>
        <div class="section-title">🍽️ Định Lượng Chỉ Số Cơ Thể & Bộ Lọc Thực Đơn</div>
        
        <div class="card-sub-title" style="margin-bottom: 5px;">⏰ Bước 1: Chọn Khung Thời Gian Khảo Sát</div>
        <div class="time-filter-grid">
            <button class="time-btn active" id="time-sang" onclick="filterByTime('sang')"><span>🌅 Buổi Sáng</span></button>
            <button class="time-btn" id="time-trua" onclick="filterByTime('trua')"><span>☀️ Buổi Trưa</span></button>
            <button class="time-btn" id="time-chieu" onclick="filterByTime('chieu')"><span>🌆 Buổi Chiều</span></button>
            <button class="time-btn" id="time-toi" onclick="filterByTime('toi')"><span>🌌 Buổi Tối/Đêm</span></button>
        </div>

        <div class="energy-time-container">
            <div id="block-energy-sang" class="status-card energy-block-item show-block" style="margin-bottom: 15px;">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#c2410c;">🌅 Định Lượng Năng Lượng Sáng</div><span id="sang-pct-text" style="font-size: 13px; font-weight: 800; color: #ff7e5f;">50%</span></div>
                <div class="stat-bar-container"><div id="sang-progress-bar" class="stat-bar-fill fill-sang" style="width: 50%;"></div></div>
                <div id="sang-status-desc" style="font-size: 11px; color: #64748b; font-weight: 600; text-align: center; margin: 4px 0;">Sáng: Bình Thường 😐</div>
                <div class="eat-btn-group">
                    <button id="btn-sang-doi" class="eat-status-btn" onclick="setTimeLevel('sang', 'doi')">🤤 Đói</button>
                    <button id="btn-sang-binhthuong" class="eat-status-btn active-warn" onclick="setTimeLevel('sang', 'binhthuong')">😐 Thường</button>
                    <button id="btn-sang-no" class="eat-status-btn" onclick="setTimeLevel('sang', 'no')">😋 No</button>
                </div>
            </div>
            <div id="block-energy-trua" class="status-card energy-block-item" style="margin-bottom: 15px;">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#15803d;">☀️ Định Lượng Năng Lượng Trưa</div><span id="trua-pct-text" style="font-size: 13px; font-weight: 800; color: #10b981;">50%</span></div>
                <div class="stat-bar-container"><div id="trua-progress-bar" class="stat-bar-fill fill-trua" style="width: 50%;"></div></div>
                <div id="trua-status-desc" style="font-size: 11px; color: #64748b; font-weight: 600; text-align: center; margin: 4px 0;">Trưa: Bình Thường 😐</div>
                <div class="eat-btn-group">
                    <button id="btn-trua-doi" class="eat-status-btn" onclick="setTimeLevel('trua', 'doi')">🤤 Đói</button>
                    <button id="btn-trua-binhthuong" class="eat-status-btn active-warn" onclick="setTimeLevel('trua', 'binhthuong')">😐 Thường</button>
                    <button id="btn-trua-no" class="eat-status-btn" onclick="setTimeLevel('trua', 'no')">😋 No</button>
                </div>
            </div>
            <div id="block-energy-chieu" class="status-card energy-block-item" style="margin-bottom: 15px;">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#a21caf;">🌆 Định Lượng Năng Lượng Chiều</div><span id="chieu-pct-text" style="font-size: 13px; font-weight: 800; color: #ec4899;">50%</span></div>
                <div class="stat-bar-container"><div id="chieu-progress-bar" class="stat-bar-fill fill-chieu" style="width: 50%;"></div></div>
                <div id="chieu-status-desc" style="font-size: 11px; color: #64748b; font-weight: 600; text-align: center; margin: 4px 0;">Chiều: Bình Thường 😐</div>
                <div class="eat-btn-group">
                    <button id="btn-chieu-doi" class="eat-status-btn" onclick="setTimeLevel('chieu', 'doi')">🤤 Đói</button>
                    <button id="btn-chieu-binhthuong" class="eat-status-btn active-warn" onclick="setTimeLevel('chieu', 'binhthuong')">😐 Thường</button>
                    <button id="btn-chieu-no" class="eat-status-btn" onclick="setTimeLevel('chieu', 'no')">😋 No</button>
                </div>
            </div>
            <div id="block-energy-toi" class="status-card energy-block-item" style="margin-bottom: 15px;">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#1e40af;">🌌 Định Lượng Năng Lượng Tối/Đêm</div><span id="toi-pct-text" style="font-size: 13px; font-weight: 800; color: #3b82f6;">50%</span></div>
                <div class="stat-bar-container"><div id="toi-progress-bar" class="stat-bar-fill fill-toi" style="width: 50%;"></div></div>
                <div id="toi-status-desc" style="font-size: 11px; color: #64748b; font-weight: 600; text-align: center; margin: 4px 0;">Tối: Bình Thường 😐</div>
                <div class="eat-btn-group">
                    <button id="btn-toi-doi" class="eat-status-btn" onclick="setTimeLevel('toi', 'doi')">🤤 Đói</button>
                    <button id="btn-toi-binhthuong" class="eat-status-btn active-warn" onclick="setTimeLevel('toi', 'binhthuong')">😐 Thường</button>
                    <button id="btn-toi-no" class="eat-status-btn" onclick="setTimeLevel('toi', 'no')">😋 No</button>
                </div>
            </div>
        </div>

        <div class="hydration-time-container" style="margin-bottom: 25px;">
            <div id="block-drink-sang" class="status-card hydration-block-item show-block">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#0369a1;">💧 Thủy Phần & Cấp Ẩm Buổi Sáng</div><span id="drink-sang-pct-text" style="font-size: 13px; font-weight: 800; color: #0284c7;">50%</span></div>
                <div class="stat-bar-container" style="height: 12px;"><div id="drink-sang-progress-bar" class="stat-bar-fill fill-drink" style="width: 50%;"></div></div>
                <div id="drink-sang-status-desc" style="font-size: 12px; color: #475569; font-weight: 600; text-align: center; margin: 4px 0 8px 0;">Trạng thái Sáng: Bình Thường 😐</div>
                <div class="eat-btn-group"><button id="btn-drink-sang-khat" class="eat-status-btn" onclick="setDrinkLevel('sang', 'khat')">🥵 Đang Khát</button><button id="btn-drink-sang-binhthuong" class="eat-status-btn active-warn" onclick="setDrinkLevel('sang', 'binhthuong')">😐 Bình Thường</button><button id="btn-drink-sang-day" class="eat-status-btn" onclick="setDrinkLevel('sang', 'day')">🐳 Đầy Nước</button></div>
            </div>
            <div id="block-drink-trua" class="status-card hydration-block-item">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#0369a1;">💧 Thủy Phần & Cấp Ẩm Buổi Trưa</div><span id="drink-trua-pct-text" style="font-size: 13px; font-weight: 800; color: #0284c7;">50%</span></div>
                <div class="stat-bar-container" style="height: 12px;"><div id="drink-trua-progress-bar" class="stat-bar-fill fill-drink" style="width: 50%;"></div></div>
                <div id="drink-trua-status-desc" style="font-size: 12px; color: #475569; font-weight: 600; text-align: center; margin: 4px 0 8px 0;">Trạng thái Trưa: Bình Thường 😐</div>
                <div class="eat-btn-group"><button id="btn-drink-trua-khat" class="eat-status-btn" onclick="setDrinkLevel('trua', 'khat')">🥵 Đang Khát</button><button id="btn-drink-trua-binhthuong" class="eat-status-btn active-warn" onclick="setDrinkLevel('trua', 'binhthuong')">😐 Bình Thường</button><button id="btn-drink-trua-day" class="eat-status-btn" onclick="setDrinkLevel('trua', 'day')">🐳 Đầy Nước</button></div>
            </div>
            <div id="block-drink-chieu" class="status-card hydration-block-item">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#0369a1;">💧 Thủy Phần & Cấp Ẩm Buổi Chiều</div><span id="drink-chieu-pct-text" style="font-size: 13px; font-weight: 800; color: #0284c7;">50%</span></div>
                <div class="stat-bar-container" style="height: 12px;"><div id="drink-chieu-progress-bar" class="stat-bar-fill fill-drink" style="width: 50%;"></div></div>
                <div id="drink-chieu-status-desc" style="font-size: 12px; color: #475569; font-weight: 600; text-align: center; margin: 4px 0 8px 0;">Trạng thái Chiều: Bình Thường 😐</div>
                <div class="eat-btn-group"><button id="btn-drink-chieu-khat" class="eat-status-btn" onclick="setDrinkLevel('chieu', 'khat')">🥵 Đang Khát</button><button id="btn-drink-chieu-binhthuong" class="eat-status-btn active-warn" onclick="setDrinkLevel('chieu', 'binhthuong')">😐 Bình Thường</button><button id="btn-drink-chieu-day" class="eat-status-btn" onclick="setDrinkLevel('chieu', 'day')">🐳 Đầy Nước</button></div>
            </div>
            <div id="block-drink-toi" class="status-card hydration-block-item">
                <div style="display: flex; justify-content: space-between; align-items: center;"><div class="card-sub-title" style="margin:0; color:#0369a1;">💧 Thủy Phần & Cấp Ẩm Buổi Tối/Đêm</div><span id="drink-toi-pct-text" style="font-size: 13px; font-weight: 800; color: #0284c7;">50%</span></div>
                <div class="stat-bar-container" style="height: 12px;"><div id="drink-toi-progress-bar" class="stat-bar-fill fill-drink" style="width: 50%;"></div></div>
                <div id="drink-toi-status-desc" style="font-size: 12px; color: #475569; font-weight: 600; text-align: center; margin: 4px 0 8px 0;">Trạng thái Tối: Bình Thường 😐</div>
                <div class="eat-btn-group"><button id="btn-drink-toi-khat" class="eat-status-btn" onclick="setDrinkLevel('toi', 'khat')">🥵 Đang Khát</button><button id="btn-drink-toi-binhthuong" class="eat-status-btn active-warn" onclick="setDrinkLevel('toi', 'binhthuong')">😐 Bình Thường</button><button id="btn-drink-toi-day" class="eat-status-btn" onclick="setDrinkLevel('toi', 'day')">🐳 Đầy Nước</button></div>
            </div>
        </div>

        <hr style="border: 0; height: 1px; background: rgba(0,0,0,0.08); margin: 25px 0;">
        <div class="card-sub-title" style="margin-bottom: 8px;">📋 Bước 2: Chọn Khẩu Vị Vùng Miền</div>
        <div class="menu-tabs">
            <button class="tab-btn active" id="tab-mienvac" onclick="switchRegionTab('mienvac')">Món Bắc Đậm Đà 🍜</button>
            <button class="tab-btn" id="tab-mientrung" onclick="switchRegionTab('mientrung')">Món Trung Cay Nồng 🍲</button>
            <button class="tab-btn" id="tab-miennam" onclick="switchRegionTab('miennam')">Món Nam Ngọt Ngào 🍧</button>
        </div>
        <div class="scroll-box"><div id="menu-display-container" class="menu-grid-items"></div></div>
    </div>


    <!-- ==================== 3. TRANG CON: TÂM TRẠNG ==================== -->
    <div id="page-mood" class="page page-mood">
        <button class="back-btn" onclick="navigateTo('page-home')">⬅️ Quay lại Trang Chủ</button>
        <div class="section-title love-title">🧠 Hệ Thống Định Vị Cảm Xúc & Phản Hồi Aura</div>
        <div class="card-sub-title">📊 Bước 1: Trạng thái cảm xúc hiện tại?</div>
        <div class="mood-grid" id="mood-selection-container">
            <div class="mood-btn" data-mood="vui" onclick="selectAdvancedMood('vui')" style="border-left: 5px solid var(--good);"><span>😊</span><span>Vui vẻ</span></div>
            <div class="mood-btn" data-mood="nhoanh" onclick="selectAdvancedMood('nhoanh')" style="border-left: 5px solid var(--love);"><span>❤️</span><span>Nhớ người yêu</span></div>
            <div class="mood-btn" data-mood="overthinking" onclick="selectAdvancedMood('overthinking')" style="border-left: 5px solid var(--info);"><span>🌀</span><span>Overthinking</span></div>
            <div class="mood-btn" data-mood="pms" onclick="selectAdvancedMood('pms')" style="border-left: 5px solid var(--danger);"><span>🩸</span><span>Nhạy cảm/PMS</span></div>
            <div class="mood-btn" data-mood="giandu" onclick="selectAdvancedMood('giandu')" style="border-left: 5px solid var(--warning);"><span>😡</span><span>Cọc cằn</span></div>
            <div class="mood-btn" data-mood="kietsuc" onclick="selectAdvancedMood('kietsuc')" style="border-left: 5px solid #334155;"><span>🔋</span><span>Cạn kiệt pin</span></div>
        </div>

        <div id="mood-advanced-panel" style="display: none; margin-top: 25px;">
            <div class="status-card" style="background: rgba(255,255,255,0.95); margin-bottom: 20px;">
                <div class="card-sub-title">🔍 Bước 2: Điều gì đã làm bạn có cảm xúc này?</div>
                <select id="mood-reason-dropdown" class="mood-box-select" onchange="handleReasonChange()">
                    <option value="">-- Chọn "thủ phạm" --</option>
                    <option value="work">💼 Áp lực công việc / Deadline dí</option>
                    <option value="love">💔 Tranh cãi / Cảm thấy bị bỏ rơi / Nhớ quá độ</option>
                    <option value="money">💸 Hết tiền / Chưa đến kỳ lương</option>
                    <option value="body">🤒 Cơ thể mệt mỏi / Thiếu ngủ</option>
                </select>
            </div>
            <div class="status-card" style="background: rgba(255,255,255,0.95); border: 1px solid rgba(0,0,0,0.05);">
                <div class="card-sub-title">🛠️ Bước 3: Phương Pháp Cải Thiện Đề Xuất</div>
                <div style="font-weight: 700; font-size: 12px; color: #475569; margin: 10px 0 6px 0;">[Tự chữa lành]</div>
                <div class="item-list" id="mood-therapy-self"></div>
                <div style="font-weight: 700; font-size: 12px; color: #b45309; margin: 18px 0 6px 0;">[Yêu cầu đối phương]</div>
                <div class="item-list" id="mood-therapy-partner"></div>
                <div style="margin-top: 25px;"><button class="btn-action-save" onclick="submitMoodReport()">🚀 Phát Tín Hiệu Cảm Xúc</button></div>
            </div>
        </div>
    </div>


    <!-- ==================== 4. TRANG CON: SỨC KHỎE & CỨU THƯƠNG ==================== -->
    <div id="page-health" class="page page-health">
        <button class="back-btn" onclick="navigateTo('page-home')">⬅️ Quay lại Trang Chủ</button>
        <div class="section-title health-title">🏥 Tình Trạng Sức Khỏe & Kết Nối Cứu Thương</div>
        
        <div class="sos-alert-box">
            <div style="font-size: 15px; font-weight: 800; color: #991b1b; margin-bottom: 6px;">🚨 KHU VỰC CỨU TRỢ KHẨN CẤP (SOS)</div>
            <div style="font-size: 12px; color: #7f1d1d; margin-bottom: 12px;">Nếu cơ thể bạn đang cực kỳ khó chịu hoặc cần sự trợ giúp ngay lập tức, hãy bấm nút dưới đây.</div>
            <button id="sos-btn" class="btn-sos-trigger" onclick="triggerSOS()">🚨 PHÁT TÍN HIỆU CỨU THƯƠNG GẦN NHẤT</button>
        </div>

        <div class="status-card" style="margin-bottom: 25px; background: rgba(255,255,255,0.95);">
            <div class="card-sub-title">📝 Thẻ ID Y Tế & Nhóm Máu</div>
            <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px;">
                <div style="background:#f1f5f9; padding: 10px; border-radius: 10px; font-size: 12px; font-weight: 700; text-align: center;">🩸 Nhóm máu: O+</div>
                <div style="background:#f1f5f9; padding: 10px; border-radius: 10px; font-size: 12px; font-weight: 700; text-align: center;">🌸 Dị ứng: Không</div>
                <div style="background:#f1f5f9; padding: 10px; border-radius: 10px; font-size: 12px; font-weight: 700; text-align: center;">💊 Tiền sử: Khỏe mạnh</div>
            </div>
        </div>

        <div class="health-grid">
            <div class="item-list">
                <div class="card-sub-title">❌ Danh mục Triệu Chứng Đau</div>
                <div class="row-item">
                    <div>Đau xương khớp 🦴 <span class="health-help-link" onclick="openEmergencyModal('dau-xuong')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Đau dạ dày 🩺 <span class="health-help-link" onclick="openEmergencyModal('dau-da-day')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Đau mỏi cơ bắp 🩹 <span class="health-help-link" onclick="openEmergencyModal('dau-co')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Đau răng / Sưng lợi 🦷 <span class="health-help-link" onclick="openEmergencyModal('dau-rang')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Đau vai gáy / Thoái hóa 🪵 <span class="health-help-link" onclick="openEmergencyModal('dau-vai-gay')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <a href="kinh-nguyet.html" class="period-link-btn">
                    <span>🩸 Đến Ngày Dâu Rụng (Xem Nhật Ký)</span>
                    <span>Xem ngay ➔</span>
                </a>
            </div>

            <div class="item-list">
                <div class="card-sub-title">🤒 Danh mục Triệu Chứng Mệt</div>
                <div class="row-item">
                    <div>Sốt cao cơ thể 🌡️ <span class="health-help-link" onclick="openEmergencyModal('sot-cao')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Cảm cúm / Sổ mũi 🤧 <span class="health-help-link" onclick="openEmergencyModal('cam-cum')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Đau đầu / Chóng mặt 🌀 <span class="health-help-link" onclick="openEmergencyModal('dau-dau')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Mỏi mắt / Khô mắt 👀 <span class="health-help-link" onclick="openEmergencyModal('moi-mat')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Tụt huyết áp / Choáng váng 📉 <span class="health-help-link" onclick="openEmergencyModal('tut-huyet-ap')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
                <div class="row-item">
                    <div>Dị ứng / Ngứa mẩn đỏ 🌸 <span class="health-help-link" onclick="openEmergencyModal('di-ung')">Cứu trợ 🚑</span></div>
                    <label class="switch"><input type="checkbox"><span class="slider-legacy"></span></label>
                </div>
            </div>
        </div>
    </div>


    <!-- ==================== 5. TRANG CON: HOẠT ĐỘNG ==================== -->
    <div id="page-act" class="page page-act">
        <button class="back-btn" onclick="navigateTo('page-home')">⬅️ Quay lại Trang Chủ</button>
        <div class="section-title love-title">💖 Hoạt Động Hẹn Hò & Mong Muốn (Đủ 50 điều)</div>
        <div class="scroll-box" style="max-height: 450px;"><div class="activity-grid" id="activity-box"></div></div>
    </div>


    <!-- ==================== 6. ĐÃ BỔ SUNG: TRANG CON TÀI CHÍNH & QUỸ CHUNG ==================== -->
    <div id="page-money" class="page page-money">
        <button class="back-btn" onclick="navigateTo('page-home')">⬅️ Quay lại Trang Chủ</button>
        <div class="section-title money-title">💵 Ví Tài Chính & Quỹ Hẹn Hò Chung</div>
        
        <div class="wallet-card">
            <div style="font-size: 12px; opacity: 0.85; text-transform: uppercase; letter-spacing: 1px; font-weight: 700;">💰 Tổng số dư Quỹ hiện tại</div>
            <div class="wallet-balance" id="wallet-balance-val">1,250,000 đ</div>
            <div style="font-size: 11px; opacity: 0.9;">Vận hành theo nguyên tắc: Chia sẻ tự nguyện & Chi tiêu hợp lý 🕊️</div>
        </div>

        <div class="status-card" style="margin-bottom: 20px; background: rgba(255,255,255,0.95);">
            <div class="card-sub-title">📝 Thêm Nhanh Giao Dịch Mới</div>
            <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 8px; margin-bottom: 10px;">
                <input type="text" id="bill-title" placeholder="Ví dụ: Ăn lẩu nướng, Xem phim..." style="padding: 12px; border-radius: 12px; border: 1px solid #cbd5e1; outline: none; font-size: 13px; font-weight: 600;">
                <input type="number" id="bill-amount" placeholder="Số tiền (đ)" style="padding: 12px; border-radius: 12px; border: 1px solid #cbd5e1; outline: none; font-size: 13px; font-weight: 600;">
            </div>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 8px;">
                <button onclick="addTransaction('in')" style="background: #10b981; color: white; border: none; padding: 12px; border-radius: 12px; font-weight: 700; cursor: pointer; font-size: 12px;">➕ Đóng Góp Quỹ (+)</button>
                <button onclick="addTransaction('out')" style="background: #ef4444; color: white; border: none; padding: 12px; border-radius: 12px; font-weight: 700; cursor: pointer; font-size: 12px;">➖ Chi Tiêu Đi Chơi (-)</button>
            </div>
        </div>

        <div class="ledger-box">
            <div class="card-sub-title" style="margin-bottom: 10px;">📜 Nhật ký thu chi gần đây</div>
            <div class="item-list" id="transaction-history-container">
                <div class="row-item"><div>🍿 Vé xem phim CGV</div><span style="color:#ef4444; font-weight:700;">-180,000 đ</span></div>
                <div class="row-item"><div>🌸 Nhà gái đóng quỹ tháng 6</div><span style="color:#10b981; font-weight:700;">+500,000 đ</span></div>
                <div class="row-item"><div>🐋 Nhà trai đóng quỹ tháng 6</div><span style="color:#10b981; font-weight:700;">+500,000 đ</span></div>
            </div>
        </div>
    </div>


    <!-- ==================== 7. TRANG CON: TÂM THƯ ==================== -->
    <div id="page-letter" class="page page-letter">
        <button class="back-btn" onclick="navigateTo('page-home')">⬅️ Quay lại Trang Chủ</button>
        <div class="section-title letter-title">💌 Hòm Thư Góp Ý & Cảm Nghĩ</div>
        <div style="font-size: 14px; color: var(--text-sub); margin-bottom: 24px; line-height: 1.6;">Nơi người liên kết để lại những ghi chú, nhận xét khách quan và đề xuất những điều cần khắc phục.</div>
        <a href="#" class="letter-link-btn" onclick="alert('Đang mở form viết tâm thư...'); return false;"><span>✍️ Viết Tâm Thư & Đánh Giá</span></a>
    </div>

</div>

<script>
    // --- CANVAS PARTICLES ---
    const canvas = document.getElementById('particles-canvas'); const ctx = canvas.getContext('2d');
    let particlesArray = []; const mouse = { x: null, y: null };
    function resizeCanvas() { canvas.width = window.innerWidth; canvas.height = window.innerHeight; }
    window.addEventListener('resize', resizeCanvas); resizeCanvas();
    window.addEventListener('mousemove', (e) => { mouse.x = e.clientX; mouse.y = e.clientY; particlesArray.push(new Particle(mouse.x, mouse.y, false)); });
    window.addEventListener('click', (e) => { for(let i=0; i<12; i++) { particlesArray.push(new Particle(e.clientX, e.clientY, true)); } });

    class Particle {
        constructor(x, y, isClick) {
            this.x = x; this.y = y; this.size = Math.random() * (isClick ? 5 : 2.5) + 0.8;
            this.speedX = Math.random() * (isClick ? 3 : 1) - (isClick ? 1.5 : 0.5); this.speedY = Math.random() * (isClick ? -3 : -1) - 0.1;
            this.color = ['rgba(96, 165, 250, 0.5)', 'rgba(168, 85, 247, 0.4)', 'rgba(253, 224, 71, 0.45)'][Math.floor(Math.random() * 3)];
            this.alpha = 1; this.decay = Math.random() * 0.012 + 0.004;
        }
        update() { this.x += this.speedX; this.y += this.speedY; this.alpha -= this.decay; }
        draw() { ctx.save(); ctx.globalAlpha = this.alpha; ctx.beginPath(); ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2); ctx.fillStyle = this.color; ctx.fill(); ctx.restore(); }
    }
    function animateParticles() { ctx.clearRect(0, 0, canvas.width, canvas.height); for (let i = 0; i < particlesArray.length; i++) { particlesArray[i].update(); particlesArray[i].draw(); if (particlesArray[i].alpha <= 0) { particlesArray.splice(i, 1); i--; } } requestAnimationFrame(animateParticles); }
    animateParticles();

    // --- NAVIGATION ---
    function toggleMenuGrid() { const grid = document.getElementById('main-menu-grid'); const arrow = document.getElementById('menu-arrow'); grid.classList.toggle('open'); arrow.innerText = grid.classList.contains('open') ? '▲' : '▼'; }
    function navigateTo(pageId) { document.querySelectorAll('.page').forEach(page => page.classList.remove('active')); document.getElementById(pageId).classList.add('active'); window.scrollTo({ top: 0, behavior: 'smooth' }); }

    // --- LOGIC THANH TIẾN TRÌNH % NĂNG LƯỢNG ĐỘC LẬP TỪNG BUỔI ---
    function setTimeLevel(timeId, level) {
        const bar = document.getElementById(`${timeId}-progress-bar`); const text = document.getElementById(`${timeId}-pct-text`); const desc = document.getElementById(`${timeId}-status-desc`);
        document.querySelectorAll(`.eat-btn-group button[id^="btn-${timeId}-"]`).forEach(b => b.className = 'eat-status-btn'); const clickedBtn = document.getElementById(`btn-${timeId}-${level}`);
        let textBuoi = timeId === 'sang' ? 'Sáng' : timeId === 'trua' ? 'Trưa' : timeId === 'chieu' ? 'Chiều' : 'Tối/Đêm';
        if(level === 'doi') { bar.style.width = '15%'; text.innerText = '15%'; desc.innerText = `${textBuoi}: Đang đói rã rời 🤤`; clickedBtn.classList.add('active-danger'); }
        else if(level === 'binhthuong') { bar.style.width = '50%'; text.innerText = '50%'; desc.innerText = `${textBuoi}: Bình Thường 😐`; clickedBtn.classList.add('active-warn'); }
        else if(level === 'no') { bar.style.width = '100%'; text.innerText = '100%'; desc.innerText = `${textBuoi}: Đã no căng bụng 😋`; clickedBtn.classList.add('active-good'); }
    }

    // --- LOGIC THANH TIẾN TRÌNH % CẤP ẨM ĐỘC LẬP TỪNG BUỔI ---
    function setDrinkLevel(timeId, level) {
        const bar = document.getElementById(`drink-${timeId}-progress-bar`); const text = document.getElementById(`drink-${timeId}-pct-text`); const desc = document.getElementById(`drink-${timeId}-status-desc`);
        document.querySelectorAll(`.eat-btn-group button[id^="btn-drink-${timeId}-"]`).forEach(b => b.className = 'eat-status-btn'); const clickedBtn = document.getElementById(`btn-drink-${timeId}-${level}`);
        let textBuoi = timeId === 'sang' ? 'Sáng' : timeId === 'trua' ? 'Trưa' : timeId === 'chieu' ? 'Chiều' : 'Tối';
        if(level === 'khat') { bar.style.width = '15%'; text.innerText = '15%'; desc.innerText = `Trạng thái ${textBuoi}: Đang khát cháy cổ 🥵`; clickedBtn.classList.add('active-danger'); }
        else if(level === 'binhthuong') { bar.style.width = '50%'; text.innerText = '50%'; desc.innerText = `Trạng thái ${textBuoi}: Khô cổ vừa phải 😐`; clickedBtn.classList.add('active-warn'); }
        else if(level === 'day') { bar.style.width = '100%'; text.innerText = '100%'; desc.innerText = `Trạng thái ${textBuoi}: Đầy nước cơ thể 🐳`; clickedBtn.classList.add('active-good'); }
    }

    // --- BỘ LỌC THỰC ĐƠN ĐỒNG BỘ ---
    let currentRegion = "mienvac"; let currentTimeFilter = "sang";
    const fullMenuDatabase = [
        { name: "Phở Bò Hà Nội 🍜", region: "mienvac", time: ["sang", "toi"] }, { name: "Bún Chả 🥓", region: "mienvac", time: ["trua", "toi"] }, { name: "Bún Riêu Cua 🦀", region: "mienvac", time: ["sang", "trua"] },
        { name: "Cơm Tấm Sườn Bì Chả 🍳", region: "mientrung", time: ["sang", "toi"] }, { name: "Cơm Gà Hội An 🍗", region: "mientrung", time: ["trua", "toi"] }, { name: "Lẩu Thái Chua Cay 🌶️", region: "mientrung", time: ["toi"] },
        { name: "Bánh Mì Dân Tổ 🥖", region: "miennam", time: ["sang", "toi"] }, { name: "Bánh Tráng Trộn 🥗", region: "miennam", time: ["chieu", "toi"] }, { name: "Trà Sữa Topping 🧋", region: "miennam", time: ["sang", "trua", "chieu", "toi"] }
    ];

    function initAndRenderMenu() {
        const container = document.getElementById('menu-display-container'); container.innerHTML = "";
        fullMenuDatabase.forEach((item) => {
            const itemEl = document.createElement('div'); itemEl.className = 'row-item';
            itemEl.setAttribute('data-region', item.region); itemEl.setAttribute('data-time', item.time.join(','));
            itemEl.innerHTML = `<span>${item.name}</span><input type="checkbox" class="custom-cb">`; container.appendChild(itemEl);
        });
        applyDualMenuFilter();
    }

    function filterByTime(timeId) {
        currentTimeFilter = timeId;
        document.querySelectorAll('.time-filter-grid .time-btn').forEach(btn => btn.classList.remove('active')); document.getElementById(`time-${timeId}`).classList.add('active');
        document.querySelectorAll('.energy-time-container .energy-block-item').forEach(block => block.classList.remove('show-block')); document.getElementById(`block-energy-${timeId}`).classList.add('show-block');
        document.querySelectorAll('.hydration-time-container .hydration-block-item').forEach(block => block.classList.remove('show-block')); document.getElementById(`block-drink-${timeId}`).classList.add('show-block');
        applyDualMenuFilter();
    }

    function switchRegionTab(regionId) { currentRegion = regionId; document.querySelectorAll('.menu-tabs .tab-btn').forEach(btn => btn.classList.remove('active')); document.getElementById(`tab-${regionId}`).classList.add('active'); applyDualMenuFilter(); }
    
    function applyDualMenuFilter() {
        const items = document.querySelectorAll('#menu-display-container .row-item');
        items.forEach(item => {
            const reg = item.getAttribute('data-region'); const times = item.getAttribute('data-time').split(',');
            if (reg === currentRegion && times.includes(currentTimeFilter)) item.classList.remove('hidden'); else item.classList.add('hidden');
        });
    }

    // --- HỆ THỐNG CẨM NÀNG SƠ CỨU TẠI CHỖ ---
    const emergencyDatabase = {
        'dau-xuong': { title: "🦴 Hướng dẫn Sơ Cứu: Đau Xương Khớp", body: "1. Tránh vận động mạnh hoặc bê vác nặng ngay lập tức.<br>2. Sử dụng túi đá chườm lạnh vào vùng đau từ 15-20 phút để giảm sưng.<br>3. Nghỉ ngơi trên bề mặt phẳng, êm.<br>4. Nếu đau âm ỉ kéo dài, dùng dầu xoa bóp nhẹ nhàng hoặc tham khảo ý kiến bác sĩ để dùng thuốc giảm đau." },
        'dau-da-day': { title: "🩺 Hướng dẫn Sơ Cứu: Đau Dạ Dày", body: "1. Pha ngay một cốc nước ấm (có thể thêm chút mật ong hoặc gừng gút nếu có).<br>2. Nằm nghiêng sang bên trái hoặc nằm ngửa, kê cao gối đầu.<br>3. Không ăn đồ chua, cay, nhiều dầu mỡ hoặc uống sữa tươi lúc này.<br>4. Dùng túi chườm ấm đặt lên vùng bụng trên rốn để xoa dịu cơn co thắt." },
        'dau-co': { title: "🩹 Hướng dẫn Sơ Cứu: Đau Mỏi Cơ Bắp", body: "1. Nghỉ ngơi và thả lỏng cơ thể hoàn toàn.<br>2. Chườm ấm nếu đau do vận động quá sức, chườm lạnh nếu nghi ngờ có chấn thương/sưng bầm.<br>3. Bổ sung thêm nước uống có chứa chất điện giải hoặc chuối chín để giảm chuột rút cơ." },
        'dau-rang': { title: "🦷 Hướng dẫn Sơ Cứu: Đau Răng / Sưng Lợi", body: "1. Súc miệng kỹ bằng nước muối ấm loãng để sát khuẩn.<br>2. Dùng túi đá chườm ở phía ngoài má vùng răng bị đau.<br>3. Tuyệt đối không nhai đồ ăn cứng hoặc quá nóng/quá lạnh vào vị trí răng đau.<br>4. Đặt lịch khám nha sĩ sớm để xử lý triệt để." },
        'dau-vai-gay': { title: "🪵 Hướng dẫn Sơ Cứu: Đau Vai Gáy", body: "1. Ngồi thẳng lưng, thực hiện các động tác xoay cổ và kéo giãn cơ cổ thật nhẹ nhàng.<br>2. Tắm nước ấm dưới vòi hoa sen hoặc chườm ấm vùng cổ vai gáy để lưu thông máu.<br>3. Thay đổi tư thế làm việc, không cúi đầu xem điện thoại quá lâu." },
        'sot-cao': { title: "🌡️ Hướng dẫn Sơ Cứu: Sốt Cao Cơ Thể", body: "1. Dùng nhiệt kế đo chính xác nhiệt độ.<br>2. Nếu trên 38.5°C, uống thuốc hạ sốt theo đúng liều lượng cân nặng.<br>3. Dùng khăn ấm lau các vùng nách, bẹn, trán để hạ nhiệt vật lý.<br>4. Mặc quần áo mỏng, thoáng mát, uống nhiều nước ấm hoặc dung dịch Oresol." },
        'cam-cum': { title: "🤧 Hướng dẫn Sơ Cứu: Cảm Cúm / Sổ Mũi", body: "1. Vệ sinh mũi bằng nước muối sinh lý NaCl 0.9%.<br>2. Giữ ấm cơ thể, đặc biệt là vùng cổ và lòng bàn chân.<br>3. Uống nước gừng ấm, trà chanh mật ong.<br>4. Nghỉ ngơi tối đa, cách ly nhẹ để tránh lây nhiễm cho người xung quanh." },
        'dau-dau': { title: "🌀 Hướng dẫn Sơ Cứu: Đau Đầu / Chóng Mặt", body: "1. Nằm nghỉ ngơi ngay lập tức trong phòng tối, yên tĩnh và thoáng khí.<br>2. Thoa một chút dầu gió vào vùng thái dương và gáy, massage nhẹ nhàng.<br>3. Tránh nhìn vào màn hình điện thoại hoặc máy tính.<br>4. Uống một cốc nước lọc lớn để bù nước cho não." },
        'moi-mat': { title: "👀 Hướng dẫn Sơ Cứu: Mỏi Mắt / Khô Mắt", body: "1. Áp dụng quy tắc 20-20-20 (Nhìn xa 20 feet trong 20 giây sau mỗi 20 phút làm việc).<br>2. Nhắm mắt thư giãn 2 phút, dùng thuốc nhỏ mắt nhân tạo để cấp ẩm.<br>3. Xoa hai lòng bàn tay vào nhau cho nóng lên rồi áp nhẹ lên hốc mắt." },
        'tut-huyet-ap': { title: "📉 Hướng dẫn Sơ Cứu: Tụt Huyết Áp", body: "1. Nằm ngửa thấp đầu, kê cao chân lên gối để máu dồn về não.<br>2. Uống ngay 1 cốc nước trà gừng đặc ấm, nước đường đặc hoặc ăn một thỏi sô-cô-la ngọt.<br>3. Tránh ngồi dậy đột ngột để phòng ngừa ngất xỉu." },
        'di-ung': { title: "🌸 Hướng dẫn Sơ Cứu: Dị Ứng Thời Tiết / Mẩn Đỏ", body: "1. Tránh gãi, chà xát mạnh gây trầy xước và nhiễm trùng da.<br>2. Tắm rửa sạch sẽ bằng nước ấm vừa phải (không tắm nước quá nóng).<br>3. Mặc quần áo chất liệu cotton rộng rãi, thấm hút mồ hôi.<br>4. Tránh tiếp xúc trực tiếp với gió lạnh, bụi phấn hoa." }
    };

    function openEmergencyModal(key) {
        const modal = document.getElementById('emergency-modal'); const title = document.getElementById('modal-title-target'); const body = document.getElementById('modal-body-target');
        if (emergencyDatabase[key]) { title.innerHTML = emergencyDatabase[key].title; body.innerHTML = emergencyDatabase[key].body; modal.style.display = 'flex'; }
    }
    function closeEmergencyModal() { document.getElementById('emergency-modal').style.display = 'none'; }

    function triggerSOS() {
        const btn = document.getElementById('sos-btn');
        if(!btn.classList.contains('activating')) { btn.classList.add('activating'); btn.innerText = "🚨 ĐANG PHÁT LỆNH SOS ĐẾN HỆ THỐNG..."; alert("Hệ thống đã nhận lệnh khẩn cấp! Đã phát tín hiệu định vị và gửi thông báo khẩn đến thiết bị của Người liên kết dỗ dành ngay lập tức!"); } 
        else { btn.classList.remove('activating'); btn.innerText = "🚨 PHÁT TÍN HIỆU CỨU THƯƠNG GẦN NHẤT"; }
    }

    // --- TÂM TRẠNG NÂNG CAO ---
    let selectedMoodId = "";
    function selectAdvancedMood(moodId) {
        selectedMoodId = moodId; document.querySelectorAll('#mood-selection-container .mood-btn').forEach(btn => { btn.classList.remove('active'); btn.style.background = 'white'; btn.style.color = 'var(--text-main)'; });
        const activeBtn = event.currentTarget; activeBtn.classList.add('active'); activeBtn.style.background = 'linear-gradient(135deg, #a855f7, #7c3aed)'; activeBtn.style.color = 'white';
        document.getElementById('mood-advanced-panel').style.display = 'block'; document.getElementById('mood-reason-dropdown').value = "";
        document.getElementById('mood-therapy-self').innerHTML = `<div style="font-size:12px; color:gray; text-align:center; padding:10px;">Vui lòng chọn thủ phạm ở bước 2...</div>`;
        document.getElementById('mood-therapy-partner').innerHTML = `<div style="font-size:12px; color:gray; text-align:center; padding:10px;">Vui lòng chọn thủ phạm ở bước 2...</div>`;
    }

    function handleReasonChange() {
        const reason = document.getElementById('mood-reason-dropdown').value; const selfBox = document.getElementById('mood-therapy-self'); const partnerBox = document.getElementById('mood-therapy-partner');
        selfBox.innerHTML = ""; partnerBox.innerHTML = ""; if(!reason) return;
        let selfActions = ["Tạm tắt thông báo 15 phút  don't đụng 📵", "Đi rửa mặt vươn vai 🧘‍♀️"], partnerActions = ["Đặt mua trà sữa gửi đến liền khẩn cấp 🧋", "Nắm tay im lặng dỗ dành ôm chặt 🤗"];
        selfActions.forEach(act => { selfBox.innerHTML += `<div class="row-item"><span>${act}</span><input type="checkbox" class="custom-cb"></div>`; });
        partnerActions.forEach(act => { partnerBox.innerHTML += `<div class="row-item"><span style="color:#b45309; font-weight:600;">${act}</span><input type="checkbox" class="custom-cb"></div>`; });
    }
    function submitMoodReport() { alert("Gửi báo cáo cảm xúc Aura thành công!"); document.getElementById('mood-advanced-panel').style.display = 'none'; }

    // --- LOGIC VÍ QUỸ CHUNG ---
    let currentBalance = 1250000;
    function addTransaction(type) {
        const titleInput = document.getElementById('bill-title'); const amountInput = document.getElementById('bill-amount');
        const title = titleInput.value.trim(); const amount = parseInt(amountInput.value);
        if(!title || isNaN(amount) || amount <= 0) { alert("Vui lòng điền đầy đủ tên khoản thu/chi và số tiền hợp lệ!"); return; }
        
        const historyContainer = document.getElementById('transaction-history-container');
        const newRow = document.createElement('div'); newRow.className = 'row-item';
        
        if (type === 'in') {
            currentBalance += amount;
            newRow.innerHTML = `<div>🌸 ${title}</div><span style="color:#10b981; font-weight:700;">+${amount.toLocaleString('vi-VN')} đ</span>`;
        } else {
            currentBalance -= amount;
            newRow.innerHTML = `<div>💸 ${title}</div><span style="color:#ef4444; font-weight:700;">-${amount.toLocaleString('vi-VN')} đ</span>`;
        }
        
        document.getElementById('wallet-balance-val').innerText = `${currentBalance.toLocaleString('vi-VN')} đ`;
        historyContainer.insertBefore(newRow, historyContainer.firstChild);
        titleInput.value = ""; amountInput.value = "";
    }

    // --- HOẠT ĐỘNG KHỞI TẠO ---
    const activities = ["Call video nhìn mặt nhau 📱", "Được anh ôm thật chặt từ phía sau 🤗", "Đi cà phê view lãng mạn ☕", "Ăn sập tiệm lẩu nướng yêu thích 🍢", "Cùng đi xem phim rạp ghế đôi 🎬", "Đi dạo phố hóng gió đêm bằng xe máy 🛵", "Được anh xoa đầu và cưng chiều 🥺", "Cùng nấu một bữa tối ấm cúng 🍳", "Được anh sấy tóc cho 💇‍♀️", "Viết thư tay gửi cho đối phương ✉️"];
    const actBox = document.getElementById('activity-box'); activities.forEach(act => { actBox.innerHTML += `<div class="row-item"><span>${act}</span><input type="checkbox" class="custom-cb"></div>`; });

    function updateClock() { const now = new Date(); document.querySelectorAll('.clock-display').forEach(el => el.innerText = now.toLocaleTimeString('vi-VN', { hour12: false })); }
    setInterval(updateClock, 1000); updateClock();
    window.onload = () => { initAndRenderMenu(); };
</script>
</body>
</html>
