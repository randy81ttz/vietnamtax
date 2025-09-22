<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>베트남 수출 의사결정 시뮬레이터 (Pro)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;500;700&display=swap');
        :root {
            --pwc-orange: #EB8C00;
            --pwc-pink: #D04A02;
            --pwc-dark-grey: #333333;
            --pwc-medium-grey: #555555;
            --pwc-light-grey: #f3f4f6;
        }
        body { font-family: 'Noto Sans KR', sans-serif; background-color: var(--pwc-light-grey); color: var(--pwc-dark-grey); }
        .app-container { width: 100%; max-width: 450px; height: 90vh; max-height: 850px; background-color: #ffffff; display: flex; flex-direction: column; overflow: hidden; }
        .screen { display: none; }
        .screen.active { display: flex; flex-direction: column; height: 100%; }
        .app-header { background-color: var(--pwc-dark-grey); color: white; flex-shrink: 0; text-align: center; }
        .app-content { flex-grow: 1; overflow-y: auto; padding: 1.5rem; }
        .progress-tracker {
            display: flex;
            gap: 0.5rem;
            padding: 0.75rem 1.5rem;
            background-color: #f9fafb;
            border-bottom: 1px solid #e5e7eb;
            flex-shrink: 0;
        }
        .progress-step {
            flex: 1;
            text-align: center;
            padding: 0.5rem;
            background-color: #e5e7eb;
            color: #6b7280;
            border-radius: 0.375rem;
            font-size: 0.75rem;
            font-weight: 500;
            transition: all 0.3s ease;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .progress-step.active { background-color: var(--pwc-orange); color: white; }
        .progress-step.completed { background-color: var(--pwc-dark-grey); color: white; }
        
        .choice-btn {
            background-color: white; color: var(--pwc-dark-grey); border: 2px solid #e5e7eb; transition: all 0.3s ease; text-align: left; padding: 1rem; width: 100%; border-radius: 0.5rem; margin-bottom: 1rem; font-weight: 500;
        }
        .choice-btn:hover { border-color: var(--pwc-orange); background-color: #fffaf0; }
        
        .result-card { background-color: #f9f9f9; border-left: 5px solid; padding: 1rem; border-radius: 0.5rem; margin-bottom: 1rem; }
        .result-card.safe { border-color: #4CAF50; }
        .result-card.warning { border-color: var(--pwc-orange); }
        .result-card.danger { border-color: var(--pwc-pink); }
        .result-title { font-weight: 700; font-size: 1.1rem; margin-bottom: 0.5rem; display: flex; align-items: center; }
        .result-title svg { margin-right: 0.5rem; width: 24px; height: 24px; }
        
        .action-btn { background-color: var(--pwc-orange); color: white; font-weight: 700; width: 100%; padding: 0.75rem; border-radius: 0.5rem; transition: background-color 0.3s; }
        .action-btn:hover { background-color: var(--pwc-pink); }
        
        .guideline-section h3 { font-size: 1.25rem; font-weight: 700; color: var(--pwc-orange); margin-bottom: 0.75rem; }
        .guideline-section p { margin-bottom: 1rem; }
        .guideline-section .highlight { background-color: #fffaf0; padding: 0.2rem 0.4rem; border-radius: 0.25rem; font-weight: 600; }
        table { width: 100%; border-collapse: collapse; margin-top: 1rem; }
        th, td { border: 1px solid #e5e7eb; padding: 0.75rem; text-align: left; font-size: 0.875rem; }
        th { background-color: #f9fafb; font-weight: 700; }
    </style>
</head>
<body class="flex items-center justify-center min-h-screen p-4">
    <div class="app-container rounded-lg shadow-lg border">
        <!-- Main Screen -->
        <div id="main-screen" class="screen active">
            <div class="app-header p-4">
                <h1 class="text-xl font-bold">베트남 수출 의사결정 시뮬레이터</h1>
            </div>
            <div class="app-content flex flex-col justify-center items-center text-center">
                <h2 class="text-3xl font-bold mb-4">어떤 계약이<br>우리 회사에 이익일까?</h2>
                <p class="text-gray-600 mb-6">계약 방식 선택이 세금과 회계에 미치는 영향을<br>직접 확인하고 최적의 전략을 찾아보세요.</p>
                <img src="https://placehold.co/300x150/EB8C00/ffffff?text=Decision+Simulation" alt="시뮬레이션 시작 이미지" class="mx-auto rounded-lg mb-6">
                <p class="text-xs text-gray-500 mb-6 p-2 bg-gray-100 rounded-md">※ 본 시뮬레이션은<br><strong>총 계약금액 5억 200만원 (기계장치 5억, 설치용역 200만원)</strong><br>거래를 가정합니다.</p>
                <button class="action-btn" onclick="showScreen('guideline-screen')">학습 후 시작하기</button>
            </div>
        </div>

        <!-- Guideline Screen -->
        <div id="guideline-screen" class="screen">
            <div class="app-header p-4"><h1 class="text-xl font-bold">시작 전 핵심 가이드라인</h1></div>
            <div class="app-content">
                <div class="guideline-section mb-6">
                    <h3>1. 외국인 계약자세 (FCT)</h3>
                    <p><strong>왜 필요할까요?</strong> 베트남 내에서 <span class="highlight text-red-600">설치와 같은 '용역'을 제공하여 발생한 소득</span>에 대해 베트남 정부가 과세하는 세금입니다. 단순히 물품만 수출(FOB, CIF 조건 등)하고 베트남 내에서 수행하는 용역이 없다면 FCT는 과세되지 않습니다.</p>
                    <p>FCT는 VAT(부가가치세)와 CIT(법인세)의 조합이며, 계약서에 거래 성격을 어떻게 명시하느냐에 따라 세율이 극적으로 달라집니다.</p>
                    <p class="text-sm p-4 bg-yellow-50 border border-yellow-200 rounded-md"><strong>'일반 서비스'란?</strong> 계약서 내용이 불명확하여 기계 공급과 설치를 구분할 수 없을 때, <span class="font-bold">베트남 과세당국</span>이 법을 가장 보수적으로 해석하여 계약 전체를 '일반 서비스'로 볼 수 있습니다. 이 경우, 가장 높은 세율(10%)이 적용되는 최악의 리스크를 의미합니다.</p>
                </div>
                 <div class="guideline-section mb-6">
                    <h4>기계장치 수출 관련 FCT 세율</h4>
                     <table>
                        <thead><tr><th>거래 유형</th><th>VAT</th><th>CIT</th></tr></thead>
                        <tbody>
                            <tr><td>1) 베트남 내 재화 공급 또는 유관 서비스 제공</td><td>-</td><td>1%</td></tr>
                             <tr><td>2) 용역</td><td>5%</td><td>5%</td></tr>
                            <tr><td>3) 자재/설비 공급 없는 건설 및 설치 용역</td><td>3%</td><td>2%</td></tr>
                            <tr><td>4) 자재/설비 공급과 함께 제공되는 건설 및 설치 용역</td><td>3%</td><td>2%</td></tr>
                        </tbody>
                    </table>
                </div>
                <div class="guideline-section mb-6">
                    <h3>2. 개인소득세 (PIT)</h3>
                    <p><strong>왜 필요할까요?</strong> 외국인(우리 직원)이 베트남 영토 내에서 일을 해서 소득이 발생하면, 그 소득에 대해 베트남 정부에 세금을 내야 합니다. 핵심은 <span class="highlight text-red-600">누가 실제로 설치 업무를 수행하느냐</span>입니다.</p>
                </div>
                 <div class="guideline-section">
                    <h3>핵심 요약표</h3>
                    <table>
                        <thead>
                            <tr><th>구분</th><th>FCT (회사 세금)</th><th>PIT (직원 세금)</th></tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>최선책</strong><br>(계약서 2개 분리)</td>
                                <td><strong class="text-green-600">최소화</strong><br>(설비 1%, 용역 5%)</td>
                                <td rowspan="3"><strong>선택에 따라 다름</strong><br>현지 위탁: 0%<br>직접 파견: 20%</td>
                            </tr>
                            <tr>
                                <td><strong>차선책</strong><br>(단일계약, 금액분리)</td>
                                <td><strong class="text-yellow-600">리스크 존재</strong><br>일반적: (설비 1%, 용역 5%)<br>최악: 전체 10%</td>
                            </tr>
                            <tr>
                                <td><strong>위험</strong><br>(턴키 계약)</td>
                                <td><strong class="text-red-600">높음</strong><br>(계약 전체에 5%)</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            <div class="p-4 border-t"><button class="action-btn" onclick="startSimulation()">이해했습니다, 시뮬레이션 시작</button></div>
        </div>

        <!-- Simulation Screen -->
        <div id="simulation-screen" class="screen">
            <div class="app-header p-4"><h1 class="text-xl font-bold">의사결정 시뮬레이션</h1></div>
            <div id="progress-tracker" class="progress-tracker">
                <div id="progress-1" class="progress-step">STEP 1</div>
                <div id="progress-2" class="progress-step">STEP 2</div>
                <div id="progress-3" class="progress-step">STEP 3</div>
            </div>
            <div class="app-content">
                <!-- Step 1: Contract -->
                <div id="step-1" class="step-content active">
                    <h2 class="text-xl font-bold mb-2">STEP 1: 계약 방식 선택</h2>
                    <p class="text-gray-600 mb-6">어떤 방식으로 계약을 체결하시겠습니까?</p>
                    <button class="choice-btn" onclick="handleChoice('contract', 'best', '[최선책] 계약 분리')">
                        <strong class="text-green-600">[최선책] 계약서 2개로 완전 분리</strong>
                        <p class="text-sm text-gray-500 mt-1">'기계 공급'과 '설치 용역' 계약서를 각각 별도로 작성합니다.</p>
                    </button>
                    <button class="choice-btn" onclick="handleChoice('contract', 'alternative', '[차선책] 금액 분리')">
                        <strong class="text-yellow-600">[차선책] 단일 계약서에 금액 분리</strong>
                        <p class="text-sm text-gray-500 mt-1">하나의 계약서에 기계 가격과 설치비를 명확히 구분하여 기재합니다.</p>
                    </button>
                    <button class="choice-btn" onclick="handleChoice('contract', 'danger', '[위험] 턴키 계약')">
                        <strong class="text-red-600">[위험] '턴키' 조건 통합 계약</strong>
                        <p class="text-sm text-gray-500 mt-1">설치까지 모든 책임을 지는 조건으로, 하나의 계약서에 통합하여 작성합니다.</p>
                    </button>
                </div>
                <!-- Step 2: Risk -->
                <div id="step-2" class="step-content" style="display:none;">
                     <h2 class="text-xl font-bold mb-2">STEP 2: 과세 리스크 관리</h2>
                    <p class="text-gray-600 mb-6">'차선책' 선택 시, 과세당국의 해석을 어떻게 가정하시겠습니까?</p>
                    <button class="choice-btn" onclick="handleChoice('risk', 'optimistic', '[실무적] 분리과세')">
                        <strong class="text-green-600">[실무적 관점] 분리과세 인정</strong>
                        <p class="text-sm text-gray-500 mt-1">일반적인 경우로, '경제적 실질'에 따라 분리과세가 될 것으로 가정합니다.</p>
                    </button>
                    <button class="choice-btn" onclick="handleChoice('risk', 'conservative', '[보수적] 통합과세')">
                        <strong class="text-red-600">[보수적 관점] 통합과세 적용</strong>
                        <p class="text-sm text-gray-500 mt-1">최악의 경우로, 계약 전체에 높은 세율이 적용될 리스크에 대비합니다.</p>
                    </button>
                </div>
                <!-- Step 3: Installation -->
                <div id="step-3" class="step-content" style="display:none;">
                    <h2 class="text-xl font-bold mb-2">STEP 3: 설치 주체 선택</h2>
                    <p class="text-gray-600 mb-6">현지 설치 작업은 누가 수행하게 할까요?</p>
                    <button class="choice-btn" onclick="handleChoice('installation', 'local', '[PIT 없음] 현지 위탁')">
                        <strong class="text-green-600">베트남 현지 관계사 위탁</strong>
                        <p class="text-sm text-gray-500 mt-1">베트남 현지 법인/협력사에 설치를 맡깁니다. (PIT 없음)</p>
                    </button>
                    <button class="choice-btn" onclick="handleChoice('installation', 'hq', '[PIT 발생] 직접 파견')">
                        <strong class="text-blue-600">한국 본사 직원 직접 파견</strong>
                        <p class="text-sm text-gray-500 mt-1">본사 기술팀이 베트남으로 출장을 가서 직접 설치를 진행합니다. (PIT 20% 발생)</p>
                    </button>
                </div>
                <!-- Result -->
                <div id="step-result" class="step-content" style="display:none;">
                    <h2 class="text-xl font-bold mb-4">최종 시뮬레이션 결과</h2>
                    <div id="result-content"></div>
                    <button class="action-btn mt-6" onclick="restartSimulation()">처음부터 다시하기</button>
                </div>
            </div>
        </div>
    </div>

<script>
    const userChoices = { contract: null, risk: null, installation: null };
    const icons = {
        safe: `<svg class="text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>`,
        warning: `<svg class="text-yellow-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>`,
        danger: `<svg class="text-red-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>`,
        info: `<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>`,
        accounting: `<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 7h6m0 10v-3m-3 3h3m-3-10h.01M9 14h.01M12 14h.01M15 14h.01M12 7v3m0 4h.01M4 7h16a2 2 0 012 2v10a2 2 0 01-2 2H4a2 2 0 01-2-2V9a2 2 0 012-2z"></path></svg>`
    };

    function showScreen(screenId) {
        document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
        document.getElementById(screenId).classList.add('active');
    }

    function showStep(stepId) {
        document.querySelectorAll('.step-content').forEach(s => s.style.display = 'none');
        document.getElementById(stepId).style.display = 'block';
        document.getElementById(stepId).classList.add('active');
    }
    
    function updateProgress(step, text) {
        const progress_el = document.getElementById(`progress-${step}`);
        if(text) {
             progress_el.textContent = text;
             progress_el.classList.add('completed');
             progress_el.classList.remove('active');
        } else {
            progress_el.classList.add('active');
        }
        for(let i = 1; i < step; i++) {
            document.getElementById(`progress-${i}`).classList.remove('active');
        }
    }

    function startSimulation() {
        showScreen('simulation-screen');
        showStep('step-1');
        updateProgress(1, null);
    }
    
    function handleChoice(stepKey, value, text) {
        userChoices[stepKey] = value;
        
        if (stepKey === 'contract') {
            updateProgress(1, text);
            if (value === 'alternative') {
                showStep('step-2');
                updateProgress(2, null);
            } else {
                userChoices.risk = null;
                updateProgress(2, '해당 없음');
                showStep('step-3');
                updateProgress(3, null);
            }
        } else if (stepKey === 'risk') {
            updateProgress(2, text);
            showStep('step-3');
            updateProgress(3, null);
        } else if (stepKey === 'installation') {
            updateProgress(3, text);
            generateResult();
            showStep('step-result');
        }
    }

    function generateResult() {
        let resultData = {};
        // FCT
        if (userChoices.contract === 'best') {
            resultData.fct = { level: 'safe', amount: '약 510만원', details: '설비가 1% (500만원), 용역비 5% (10만원)'};
        } else if (userChoices.contract === 'alternative') {
            if (userChoices.risk === 'optimistic') {
                 resultData.fct = { level: 'warning', amount: '약 510만원', details: '설비가 1% (500만원), 용역비 5% (10만원)'};
            } else {
                 resultData.fct = { level: 'danger', amount: '약 5,200만원', details: '계약 총액 5억 200만원에 10%(VAT 5%+CIT 5%) 일괄 적용'};
            }
        } else { // danger (turnkey)
            resultData.fct = { level: 'danger', amount: '약 2,600만원', details: '계약 총액 5억 200만원에 5%(VAT 3%+CIT 2%) 일괄 적용'};
        }
        // PIT
        if (userChoices.installation === 'hq') {
            resultData.pit = { level: 'warning', details: '<strong>발생 (약 40만원)</strong><br>- 용역비(200만원)를 과세소득으로 간주, 20% 세율 적용'};
        } else {
            resultData.pit = { level: 'safe', details: '<strong>발생 없음</strong>'};
        }
        // Revenue
        if (userChoices.contract === 'danger') {
            resultData.revenue = { level: 'danger', details: '<strong>통합 인식 (매출 인식 지연)</strong><br>- 전체 매출 (5억 200만원)을 설치 및 최종 검수 완료 시점에 한 번에 인식'};
            resultData.docs = { details: '<strong>- 계약서:</strong> \'완성된 시스템\' 공급 계약으로 단일 작성<br><strong>- 인보이스:</strong> 계약 총액으로 단일 발행<br><strong>- 수출신고필증:</strong> 총액 중 합리적으로 배분된 기계장치 금액(5억)만 신고'};
        } else {
            resultData.revenue = { level: 'safe', details: '<strong>분리 인식</strong><br>- 설비 매출 (5억): 선적 시점<br>- 용역 매출 (200만원): 설치 완료 시점'};
            if(userChoices.contract === 'best'){
                resultData.docs = { details: '<strong>- 계약서:</strong> 기계 공급 / 설치 용역 2건으로 분리 작성<br><strong>- 인보이스:</strong> 계약서에 맞춰 2건으로 분리 발행<br><strong>- 수출신고필증:</strong> 기계장치 공급분(5억)에 대해서만 신고'};
            } else {
                resultData.docs = { details: '<strong>- 계약서:</strong> 단일 계약서 내에 설비/용역 금액, 내용, 의무를 명확히 구분하는 조항 필수<br><strong>- 인보이스:</strong> 한 장에 발행하되, 설비/용역 항목 분리 기재<br><strong>- 수출신고필증:</strong> 기계장치 공급분(5억)에 대해서만 신고'};
            }
        }
        // Accounting for outsourcing
        if (userChoices.installation === 'local') {
            if (userChoices.contract === 'danger') {
                 resultData.accounting = { details: '현지 관계사에 지급하는 위탁수수료는 전체 <strong class="text-red-600">\'매출원가\'</strong> 계정으로 처리합니다.'};
            } else {
                 resultData.accounting = { details: '현지 관계사에 지급하는 위탁수수료는 <strong class="text-green-600">\'용역매출원가\'</strong> 계정으로 처리하여 관련 용역매출에 직접 대응시킵니다.'};
            }
        }
        
        const resultContent = document.getElementById('result-content');
        let accountingHtml = '';
        if(resultData.accounting) {
            accountingHtml = `
            <div class="result-card info">
                <div class="result-title">${icons.accounting}<span>현지 위탁수수료 회계처리</span></div>
                <p class="text-sm">${resultData.accounting.details}</p>
            </div>`;
        }
        
        resultContent.innerHTML = `
            <div class="result-card ${resultData.fct.level}">
                <div class="result-title">${icons[resultData.fct.level]}<span>FCT (외국인 계약자세)</span></div>
                <p class="text-lg font-bold text-red-600">${resultData.fct.amount}</p><p class="text-sm">${resultData.fct.details}</p>
            </div>
             <div class="result-card ${resultData.pit.level}">
                <div class="result-title">${icons[resultData.pit.level]}<span>PIT (개인소득세)</span></div>
                <p class="text-sm">${resultData.pit.details}</p>
            </div>
            <div class="result-card ${resultData.revenue.level}">
                <div class="result-title">${icons[resultData.revenue.level]}<span>수익 인식 (회계)</span></div>
                <p class="text-sm">${resultData.revenue.details}</p>
            </div>
             <div class="result-card info">
                <div class="result-title">${icons.info}<span>핵심 서류 처리 방안</span></div>
                <p class="text-sm">${resultData.docs.details}</p>
            </div>
            ${accountingHtml}
        `;
    }

    function restartSimulation() {
        Object.keys(userChoices).forEach(key => userChoices[key] = null);
        document.querySelectorAll('.progress-step').forEach((el, i) => {
            el.textContent = `STEP ${i+1}`;
            el.className = 'progress-step';
        });
        showScreen('main-screen');
    }
</script>
</body>
</html>
