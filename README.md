<!-- 五張固定橫式卡牌版位 -->

<div class="board" id="board">

    <!-- CARD 1 -->

    <div class="card">

        <div class="inner">

            <!-- 卡背 -->

            <div class="front">

                <h2>CARD 1</h2>
                <p>點擊翻牌</p>

            </div>

            <!-- 卡面 -->

            <div class="back">

                <img src="images/demo1.jpg">

                <div class="overlay"></div>

                <div class="card-title">

                    男子講電話

                </div>

                <div class="card-controls">

                    <button>⬅ 左移</button>

                    <button>右移 ➡</button>

                </div>

            </div>

        </div>

    </div>

    <!-- CARD 2 -->

    <div class="card">

        <div class="inner">

            <div class="front">

                <h2>CARD 2</h2>
                <p>點擊翻牌</p>

            </div>

            <div class="back">

                <img src="images/demo2.jpg">

                <div class="overlay"></div>

                <div class="card-title">

                    打開門

                </div>

                <div class="card-controls">

                    <button>⬅ 左移</button>

                    <button>右移 ➡</button>

                </div>

            </div>

        </div>

    </div>

    <!-- CARD 3 -->

    <div class="card">

        <div class="inner">

            <div class="front">

                <h2>CARD 3</h2>
                <p>點擊翻牌</p>

            </div>

            <div class="back">

                <img src="images/demo3.jpg">

                <div class="overlay"></div>

                <div class="card-title">

                    街道上的貓

                </div>

                <div class="card-controls">

                    <button>⬅ 左移</button>

                    <button>右移 ➡</button>

                </div>

            </div>

        </div>

    </div>

    <!-- CARD 4 -->

    <div class="card">

        <div class="inner">

            <div class="front">

                <h2>CARD 4</h2>
                <p>點擊翻牌</p>

            </div>

            <div class="back">

                <img src="images/demo4.jpg">

                <div class="overlay"></div>

                <div class="card-title">

                    微笑

                </div>

                <div class="card-controls">

                    <button>⬅ 左移</button>

                    <button>右移 ➡</button>

                </div>

            </div>

        </div>

    </div>

    <!-- CARD 5 -->

    <div class="card">

        <div class="inner">

            <div class="front">

                <h2>CARD 5</h2>
                <p>點擊翻牌</p>

            </div>

            <div class="back">

                <img src="images/demo5.jpg">

                <div class="overlay"></div>

                <div class="card-title">

                    女子流淚

                </div>

                <div class="card-controls">

                    <button>⬅ 左移</button>

                    <button>右移 ➡</button>

                </div>

            </div>

        </div>

    </div>

</div>

<style>

/* 五張固定橫式版位 */

.board{

    display:grid;

    grid-template-columns:1fr;

    gap:25px;

    max-width:1400px;

    margin:auto;

}

/* 卡牌 */

.card{

    perspective:1000px;

    width:100%;

    aspect-ratio:16 / 9;

}

/* 翻牌 */

.inner{

    position:relative;

    width:100%;
    height:100%;

    transition:0.8s;

    transform-style:preserve-3d;

}

/* 卡面 */

.front,
.back{

    position:absolute;

    width:100%;
    height:100%;

    border-radius:24px;

    overflow:hidden;

    backface-visibility:hidden;

}

/* 卡背 */

.front{

    background:
    linear-gradient(
        135deg,
        #1e293b,
        #0f172a
    );

    border:3px solid #475569;

    display:flex;

    justify-content:center;
    align-items:center;

    flex-direction:column;

    color:white;

}

/* 卡面 */

.back{

    background:#111827;

    transform:rotateY(180deg);

}

/* 圖片 */

.back img{

    width:100%;
    height:100%;

    object-fit:cover;

}

/* 底部黑色漸層 */

.overlay{

    position:absolute;

    left:0;
    right:0;
    bottom:0;

    height:45%;

    background:linear-gradient(
        transparent,
        rgba(0,0,0,0.85)
    );

}

/* 標題 */

.card-title{

    position:absolute;

    left:20px;
    bottom:70px;

    color:white;

    font-size:28px;
    font-weight:bold;

    text-shadow:0 3px 10px rgba(0,0,0,0.7);

}

/* 控制按鈕 */

.card-controls{

    position:absolute;

    left:20px;
    right:20px;
    bottom:18px;

    display:flex;

    gap:10px;

}

.card-controls button{

    flex:1;

    border:none;

    padding:12px;

    border-radius:14px;

    background:rgba(255,255,255,0.15);

    color:white;

    cursor:pointer;

    backdrop-filter:blur(8px);

}

.card-controls button:hover{

    background:rgba(255,255,255,0.3);

}

body{

    background:#0f172a;

    padding:30px;

    font-family:"Microsoft JhengHei";

}

</style>
