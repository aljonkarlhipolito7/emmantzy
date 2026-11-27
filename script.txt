/* =====================================================
   OUR STORY — script.js
   -----------------------------------------------------
   EDIT HERE: the password, the 10 memories and the love letter.
   Everything else in this file can be left alone.

   TIP: write your texts between backticks ( ` ` ).
   Inside backticks you can freely use "quotes", 'apostrophes'
   and press Enter for a new line.
   ===================================================== */

/* ---------- 0. PASSWORD (6 digits only) ---------- */
const PASSWORD = "120125";

/* ---------- 1. YOUR 10 MEMORIES (edit these!) ---------- */
const memories = [
  {
    image: "pic1.jfif",
    title: "The Day Our Story Began",
    date: "12/12/25",
    caption: "Where everything quietly began.",
    story: `itu yung unang labas natin together, masaya na medyo kabado bente kasi kasi (HAHAHAHA) but still masaya, panahon pamasahe lang dala natin tas nag dadala nalang us ng foods, literal na zero days he. sobrang saya ko yan kasi kasama kita tas na side hug pa kita kasi hiyaa aku ihhh, and diko alam na mag mamahal na pala ulit ako and diko sure if mananalo ba ako or anu pero kasi uk me una palang sugal sya he "susugal ako kahit walang kasiguraduhan" tlagang sheshh he HAHAHAHAHAH.`,
    message: `Thank you for walking into my life. I'm so glad it was you.`
  },
  {
    image: "pic2.jfif",
    title: "One Message Away",
    date: "12/01/25",
    caption: "Who knew one message could lead to us?.",
    story: `grabe kaba ko ditu as in kung alam mo lang, kasi dipa naman tayo ganon ka close talagang nilakasan ko lang loob ko he literal na "bahala na si superman" HAHAHAHA) ayun success naman nag response naman agad syaa and nag tuloy tuloy hanggang sa nag click agad sila, fam prob banaman topic he relate sila both HAHAHAHA, until now can't imagine na nandito tayo ngayon pano nalang kaya kung di ako nag chat sayo no? wala ka sigurong bf na loyal na mabait? HAHAHAHAHAHAHAHA.`,
    message: `If I never sent that message, I wouldn't have us. And I'm glad I did.`
  },
  {
    image: "pic3.jfif",
    title: "A Little Piece of You",
    date: "12/12/26",
    caption: "Worn out, but never thrown away..",
    story: `bohaii padin syaa itu yung unang things na binigay mo sakin na sayo mismo galing kaya sobrang kinikeep ko syaa, nasa wallet ko padin sya kasi sobrang himolmol na but still naka keep padin sya kasi galing sya sayoo and itung suot ko now medyo matibay tibay sya sayo pading galing to kasi nga himulmol malala na yung na una HAHAHHA, it's remember me na sayo ako (anuuu sayo ako?!?! HAHAHA) deh yun naman kasi talaga purpose non, kaya sobrang mahalaga sakin to it's always reminds me of u lalo't galing pa sayo🫰🫰.`,
    message: `It's not just a gift, it's a little reminder of you that I always carry with me.`
  },
  {
    image: "pic4.jfif",
    title: "Our First Real Date",
    date: "03/26/26",
    caption: "Months of missed celebrations, all in one day.",
    story: `Titu lang yung first natin na labas na bond talaga kasi maingat pa sila nong 3months ngayon malalaks na haha, dito tayo bumawi ng pics ng mga monthsary natin na nag daan na di tayo nakapag celeb kasi mabait pa tayo non hahah, kaya for me itu yung our first day especial day natin kasi marami tayong pics yan na kuket dibaa dibaa photoboth lalo sa earts non.`,
    message: `I love how even the simplest dates with you become special. Here's to more pictures, dates, and memories together.`
  },
  {
    image: "pic5.jfif",
    title: "Still Here, Still Us",
    date: "01/07/26",
    caption: "We were just making plans, but look at us now.",
    story: `so yunn katatapos mo lang umiyak dito HAHAHHAHAHAHA, lumabas tayo yan iniwan natin sila nag pahangin us first time mong umiyak sakin abt life n us. and dun na nabuo lahat ng dreams natin together also the bond that day sobrang sayaa kasi parang kahapon lang sya pero look mag ooneyear nayan silaa, can't believe parin akii parang plans lang natin to noon sa araw ng pics nayan and look we're still here 🤗.`,
    message: `t feels like yesterday when we were just talking about our future, and now look at us, still holding on. I'm glad we're still here, making those dreams come true together 🤗💜.`
  },
  {
    image: "pic6.jfif",
    title: "Just Us Being Us",
    date: "01/25/26",
    caption: "A little chaos, a lot of love.",
    story: `grabe tawanan natin ditu kahit nanjan tito mo, talagang patigasan ng mukha e nag tt payan sila tas vvid vid talaga sheshh, masaya tayo yan kasi last day kuno?? kung baga nilubos lunod na he pero mag oone year na HHAHAHAH wala e mahal na mahal he, grabe tawanan natin jan ginagalit kasi natin tito mo jann HAHAHAHAHAHA.`,
    message: `I hope we never lose this kind of laughter, no matter how many years pass. I want more silly moments, more kulit, and more days like this with you. 💜`
  },
  {
    image: "pic7.jfif",
    title: "Learning, Loving, Growing",
    date: "03/10/26",
    caption: "We didn't always get it right, but we always tried to fix it.",
    story: `Tituu ilang days after natin mag 3moths ayun sa 3monts dun na pumasok yung mga struggles n problems natin together dun na nag start yung mga deeptalks mga hinanakit at kung ano ano pang ka ekekan nila, ayun kung saan mas naintidihan kita mas minahal mas nag pakatibay tayo. mas naunawaan ko yung sitwasyon mo and kahit ganon minsan may mga tampo us misunderstanding always nating inaayos ng maayus n sobrang thankful ako dun wabb kaya mas minamahal kita sa mahihirapan na sitwasyon.`,
    message: `I'm thankful for every deep talk, every understanding, and every time we chose to fix things. I don't expect us to be perfect, but I hope we never stop learning how to love each other better. 💜`
  },
  {
    image: "pic8.jfif",
    title: "A Dream Slowly Coming True",
    date: "05/07/26",
    caption: "Little by little, our dreams are becoming real..",
    story: `sobrang saya nitoo kasi nakapag outing sila together w fam kahit di kumpleto but still, unti unti lang wabb yung mga fantasy natin noon nagiging reality na hold lang akii hmmm 🤗 pano pa kaya kapag all goods na edi sobrang saya nayan kada may outing di na need mag tago (mag tago sa kwarto kasama si chayii para lang ma hugg) di makapag pigil he.`,
    message: `We may not have everything we want yet, but I'm happy that we're slowly getting there together. I can't wait for more outings, more hugs, and more happy days with you.`
  },
  {
    image: "pic9.jfif",
    title: "Flowers and Our First Kiss",
    date: "02/18/26",
    caption: "Flowers, hugs, and our first kiss.",
    story: `first time ko lang kasi gumawa ng flowers for girl kaya ayunn, pero syempre pinaka best memory talaag is yung first kiss natinnn 12/24/25 HAHAHAHAHA kabisado he tas nahugg pa kita ng matagal jann compare sa rob kasi bago bago palang sila pero alam mo hiya ko that timee nak tumatama he HAHAHAHAHAHHA.`,
    message: `I may have been shy, but I wouldn't change that moment for anything. It's one of those memories I'll always keep close to my heart. 💗`
  },
  {
    image: "pic10.jfif",
    title: "You, Again and Again",
    date: "07/16/26",
    caption: "No matter what, it's always you.",
    story: `again n again wabwabb ko ikaw at ikaw lang po palagi no matter what. mahal na mahal higit pa sa salitang mahal.

iloveyouuuusomuchiieee akii always.`,
    message: `Again and again, wabwabb ko, ikaw at ikaw lang po palagi. No matter what happens, I will keep choosing you. I love you more than words can ever say. Iloveyouuuusomuchiieee, akii, always.`
  }
];

/* ---------- 2. YOUR LOVE LETTER (edit these!) ----------
   Each line is one paragraph. The last one is the signature. */
const loveLetter = [
  `HAPPII ANIVERSARY AKII! 🩵✨ wahhhhh diko alam sasabihin ko real hahah 😭😭,`,
  `uhmmm... haloo akii alam kong nasabi na natin lahat together but i want to sat again n again. thankyou for always. especially kay brow alam namin po brow marami kaming false but we promised na papanalo namin to no matter what. diba akii thankyou din po for always to be center of this rs kahit pasaway yan sila hehe labyouu po 🫶🫶.`,
  `so yun akii, thankyou for trusting binigyan mo ako ng chance para mahalin ka. maging kaaliwan mo and sobrang thankful talaga ako kasi nong nakita kita noon sabi ko happy crush then ayun nag tuloy tuloy na na para bang? siguro gods plan talaga and i hope so. kasii pinag pray talaga kita sabi ko non kay brow "brow if ever man sya uk me willing to wait po ako and if ever mas aayusin ko na po" blablaa tas yun nag papansin ka sakin  HAHAHHAAH just kidding ayun nga nag tuloy tuloy na nag simula sa asaran, asaran nila hanggang sa ayun na nga nag first move na si press at nag pa impress anuu tugmaan? HAHAHAHHA hanggang ngayon di parin ako makapaniwala eh. especially sa mga Harddays natin minsan tayo na yung mag kalaban but we're still here akii..`,
  `wish ko lang satin sana lahat ng plans natin is matupad mabagal man matagal pa basta may kasiguraduhan mag wwait ako until we make it. and sana mas manaig parin satin yung love ng isa't isa lalo sa mga mas mahihirap na sitwasyon at lagi natin ayusin ng maayus di dahil kailangan kundi mahal natin yung isa't-isa like we used to be. wag nating makasanayan yung mga ganon bagay kasi hindi natin alam yung bukas na dadating malay natin isa satin mawala bigla diba, kaya i wish na always natin ayusin agad if kaya naman if need naman ng space n time diba binibigay naman natin. takot lang din akong masanay tayo sa ganon oo okay tayo pero alam natin sa sarili natin na may kulang n mali. at sana di natin baniwalain yun dahil dun nag sisimula sa maliliit hanggang sa lumaki at lumama na.`,
  `and kapag na ffeel natin na nawawala na yung love o spark uu reality pero sana always nating gawan ng paraan para mawala yung feelings nayun syempre nanjan lagi ang kalaban para guluhin us n part din ng pagsubok ng rs, kaya sana mag eefort tayo both and napag uusapan naman natin always kapag may prob, palagi lang tayong bumalik sa dati kung pano tayo nong una.`,
  `wishing u all the best dahil deserve mo yun akii, lagi mong inu-una yung ibang tao bago ikaw kaya hayaan mo kong unahin ka. alam kong dika madamot kaya deserve mo to deserve mo ng love kaya don't ask ur self if deserve mo ba to, kasi yess kaya nga binigay ako sayo ji brow (anueee bigay ni brow?!?!?? HHAHAHAHAHAHHAAH) kasi wag ng pumalag.`,
  `diko na alam sasabihin ko kasi nasabi na naman natin lahat, and kapag may nga misunderstanding naman napag uusapan and nakakapag pangaralan sila.`,
  `bastaa mahal ko ikaw, sobrang mahal na mahal na mahal always no matter. kaya no pressure okeyy tyt lang pu always, parehas tayong matotoo ng sabay and be the best for us. di man ngayon bat soon.`,
  `hold lang akii hmmm like what we always said pu, fighting lang akii here lang ako for u, basta diba po wag mag papabaya and always kakain sa oras at mag papahinga kaya plss always takecare pu wabwabb hanii and uminom lagi ng maraming watohh para bati tayo, bawasan katigasan ng ulo kapag bawal bawal pu hani. kahinhinan at mga bawal sayo. kukurutin kita jan tamo nigagalit mo talaga si dada ayytt. mahal ko ikaw kaya wag nag papabaya.`,
  `happii aniversary!! 💞 iloveyouuuuuu palagii.`,
  `- akii 💜 \u2661`
];

/* =====================================================
   ENGINE — you do not need to edit anything below
   ===================================================== */
(function () {
  'use strict';

  const TOTAL = memories.length;
  const LAYOUTS = ['a', 'b', 'c', 'd'];
  const FRAMES = ['polaroid', 'mat', 'tape'];
  const reduceMotion = !!(window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches);

  const $ = (id) => document.getElementById(id);
  const pad = (n) => String(n).padStart(2, '0');
  const rand = (min, max) => Math.random() * (max - min) + min;
  const T = (ms) => (reduceMotion ? Math.round(ms * 0.15) : ms);

  /* ---------- state ---------- */
  let currentChapter = 0;
  let viewerIndex = 0;
  let chapterBusy = false;
  let journeyStarted = false;
  let pin = '';
  let lockBusy = false;
  let letterOpened = false;
  let musicPaused = false;      // true only if the visitor paused it on purpose
  let lastFocus = null;

  /* =====================================================
     IMAGES
     ===================================================== */
  function placeholder(n) {
    const svg =
      "<svg xmlns='http://www.w3.org/2000/svg' width='900' height='1100' viewBox='0 0 900 1100'>" +
      "<defs><linearGradient id='g' x1='0' y1='0' x2='1' y2='1'><stop offset='0' stop-color='#f3f9ff'/><stop offset='1' stop-color='#a9d6f5'/></linearGradient></defs>" +
      "<rect width='900' height='1100' fill='url(#g)'/>" +
      "<text x='450' y='540' font-size='200' text-anchor='middle' fill='#ffffff'>♥</text>" +
      "<text x='450' y='680' font-size='46' text-anchor='middle' fill='#1f3a5c' font-family='Georgia'>Add pic" + n + ".jfif</text>" +
      "</svg>";
    return 'data:image/svg+xml;charset=utf-8,' + encodeURIComponent(svg);
  }

  function setImage(img, index) {
    img.onerror = () => { img.onerror = null; img.src = placeholder(index + 1); };
    img.src = memories[index].image;
    img.alt = memories[index].title;
  }

  function preload(index) {
    if (index < 0 || index >= TOTAL) return;
    const im = new Image();
    im.src = memories[index].image;
  }

  /* =====================================================
     SCREENS + SMALL EFFECTS
     ===================================================== */
  function showScreen(id) {
    document.querySelectorAll('.screen').forEach((s) => {
      const on = s.id === id;
      s.classList.toggle('active', on);
      s.setAttribute('aria-hidden', on ? 'false' : 'true');
    });
    const el = $(id);
    el.scrollTop = 0;
    document.body.dataset.screen = id;
  }

  function burst(x, y, count) {
    if (reduceMotion) return;
    for (let i = 0; i < (count || 5); i++) {
      const h = document.createElement('span');
      h.className = 'click-heart';
      h.textContent = '♥';
      h.style.left = x + 'px';
      h.style.top = y + 'px';
      h.style.fontSize = rand(11, 20) + 'px';
      h.style.setProperty('--dx', rand(-70, 70) + 'px');
      h.style.setProperty('--dy', rand(-130, -50) + 'px');
      document.body.appendChild(h);
      setTimeout(() => h.remove(), 1300);
    }
  }
  function burstFrom(el, count) {
    const r = el.getBoundingClientRect();
    burst(r.left + r.width / 2, r.top + r.height / 2, count);
  }

  function heartTransition(midpoint, done) {
    const tr = $('transition');
    tr.classList.add('show');
    setTimeout(midpoint, T(750));
    setTimeout(() => { tr.classList.remove('show'); if (done) done(); }, T(1500));
  }

  /* =====================================================
     ATMOSPHERE (kept deliberately light)
     ===================================================== */
  function buildAtmosphere() {
    const stars = $('stars');
    for (let i = 0; i < 26; i++) {
      const s = document.createElement('i');
      s.className = 'star';
      s.style.cssText = `left:${rand(0, 100)}%;top:${rand(0, 100)}%;--s:${rand(1.5, 3.2).toFixed(1)}px;` +
        `animation-duration:${rand(3, 7).toFixed(1)}s;animation-delay:${(-rand(0, 7)).toFixed(1)}s;`;
      stars.appendChild(s);
    }
    const clouds = $('clouds');
    for (let i = 0; i < 5; i++) {
      const c = document.createElement('div');
      c.className = 'cloud';
      c.style.cssText = `--w:${Math.round(rand(200, 360))}px;--o:${rand(0.35, 0.7).toFixed(2)};top:${rand(2, 78).toFixed(0)}%;` +
        `animation-duration:${Math.round(rand(110, 190))}s;animation-delay:${(-rand(0, 150)).toFixed(0)}s;`;
      clouds.appendChild(c);
    }
    const particles = $('particles');
    for (let i = 0; i < 16; i++) {
      const p = document.createElement('i');
      p.className = 'particle';
      p.style.cssText = `left:${rand(0, 100)}%;--s:${Math.round(rand(4, 10))}px;` +
        `animation-duration:${Math.round(rand(16, 30))}s;animation-delay:${(-rand(0, 30)).toFixed(0)}s;`;
      particles.appendChild(p);
    }
    const box = $('hearts');
    function spawn() {
      if (document.hidden || reduceMotion || box.childElementCount >= 5) return;
      const h = document.createElement('span');
      const dur = rand(16, 24);
      h.className = 'float-heart';
      h.textContent = '♥';
      h.style.left = rand(3, 96) + '%';
      h.style.fontSize = rand(12, 22) + 'px';
      h.style.animationDuration = dur + 's';
      box.appendChild(h);
      setTimeout(() => h.remove(), dur * 1000);
    }
    setTimeout(spawn, 1200);
    setInterval(spawn, 3600);
    document.addEventListener('visibilitychange', () => document.body.classList.toggle('is-paused', document.hidden));
  }

  /* =====================================================
     PASSWORD (6 digits only)
     ===================================================== */
  function renderPin() {
    document.querySelectorAll('#pinDots span').forEach((d, i) => d.classList.toggle('on', i < pin.length));
    $('pinDots').setAttribute('aria-label', pin.length + ' of 6 digits entered');
  }
  function setMsg(text, tone) {
    const m = $('pinError');
    m.textContent = text || '';
    m.dataset.tone = tone || '';
  }
  function lockState(cls) {
    const card = $('lockCard');
    card.classList.remove('is-error', 'is-success', 'is-nudge');
    if (cls) { void card.offsetWidth; card.classList.add(cls); }
  }
  function flashKey(k) {
    const el = document.querySelector('.key[data-key="' + k + '"]');
    if (!el) return;
    el.classList.add('is-pressed');
    setTimeout(() => el.classList.remove('is-pressed'), 130);
  }

  function pressKey(k) {
    if (lockBusy || !$('lock').classList.contains('active')) return;

    if (k === 'enter') {                       // empty / incomplete feedback
      if (pin.length === 0) setMsg('Type the 6 digits first.');
      else setMsg((6 - pin.length) + ' more digit' + (pin.length === 5 ? '' : 's') + ' to go.');
      lockState('is-nudge');
      return;
    }
    setMsg('');
    lockState(null);
    if (k === 'del') pin = pin.slice(0, -1);
    else if (k === 'clear') pin = '';
    else if (/^\d$/.test(k) && pin.length < 6) pin += k;     // digits only, max 6
    renderPin();
    if (pin.length === 6) checkPin();
  }

  function checkPin() {
    lockBusy = true;
    if (pin === PASSWORD) {
      lockState('is-success');
      setMsg('Welcome in ♡', 'ok');
      tryPlayMusic();                          // inside the user's tap, so the browser allows it
      setTimeout(() => {
        showScreen('opening');
        pin = ''; renderPin(); lockState(null); setMsg('');
        lockBusy = false;
      }, T(800));
    } else {
      lockState('is-error');
      setMsg("That's not it — try again.", 'err');
      setTimeout(() => {
        pin = ''; renderPin(); lockState(null);
        lockBusy = false;
      }, T(750));
    }
  }

  function setupLock() {
    document.querySelectorAll('.key').forEach((b) =>
      b.addEventListener('click', () => pressKey(b.dataset.key)));

    document.addEventListener('keydown', (e) => {
      if (!$('lock').classList.contains('active') || e.ctrlKey || e.metaKey || e.altKey) return;
      if (/^\d$/.test(e.key)) { flashKey(e.key); pressKey(e.key); }
      else if (e.key === 'Backspace') { flashKey('del'); pressKey('del'); }
      else if (e.key === 'Escape') { flashKey('clear'); pressKey('clear'); }
      else if (e.key === 'Enter') { e.preventDefault(); pressKey('enter'); }
    });
  }

  /* =====================================================
     MUSIC
     ===================================================== */
  function tryPlayMusic() {
    const a = $('bgMusic');
    if (musicPaused || !a.paused) return;
    const p = a.play();
    if (p && p.catch) p.catch(() => {});
  }

  function setupMusic() {
    const a = $('bgMusic');
    const player = $('musicPlayer');
    const toggle = $('musicToggle');
    const mute = $('musicMute');

    function sync() {
      const on = !a.paused;
      player.classList.toggle('playing', on);
      toggle.setAttribute('aria-pressed', String(on));
      toggle.setAttribute('aria-label', on ? 'Pause music' : 'Play music');
    }
    a.addEventListener('play', sync);
    a.addEventListener('pause', sync);
    a.addEventListener('error', () => { $('musicLabel').textContent = 'Add music.mp3'; });

    toggle.addEventListener('click', () => {
      if (a.paused) {
        musicPaused = false;
        const p = a.play();
        if (p && p.catch) p.catch(() => { $('musicLabel').textContent = 'music.mp3 not found'; });
      } else {
        musicPaused = true;
        a.pause();
      }
    });
    mute.addEventListener('click', () => {
      a.muted = !a.muted;
      player.classList.toggle('muted', a.muted);
      mute.setAttribute('aria-pressed', String(a.muted));
      mute.setAttribute('aria-label', a.muted ? 'Unmute music' : 'Mute music');
    });

    // fade the little player while a page is being scrolled so it never covers the story or the letter
    let t;
    document.addEventListener('scroll', (e) => {
      if (!e.target.classList || !e.target.classList.contains('screen')) return;
      player.classList.add('is-dim');
      clearTimeout(t);
      t = setTimeout(() => player.classList.remove('is-dim'), 1000);
    }, true);
  }

  /* =====================================================
     COVER -> CHAPTERS
     ===================================================== */
  function beginJourney(e) {
    if (journeyStarted) return;
    journeyStarted = true;
    tryPlayMusic();                            // backup in case the browser blocked it earlier
    burst(e.clientX || innerWidth / 2, e.clientY || innerHeight / 2, 7);
    heartTransition(() => {
      currentChapter = 0;
      fillChapter(0);
      showScreen('chapter');
    }, () => { journeyStarted = false; });
  }

  /* =====================================================
     CHAPTERS
     ===================================================== */
  function fillChapter(i) {
    const m = memories[i];
    $('chapterContent').dataset.layout = LAYOUTS[i % LAYOUTS.length];
    $('chapterBigNo').textContent = pad(i + 1);
    $('chapterNumber').textContent = 'Chapter ' + pad(i + 1) + ' / ' + pad(TOTAL);
    $('chapterTitle').textContent = m.title;
    $('chapterDate').textContent = m.date;
    $('chapterStory').textContent = m.story;
    $('chapterMessage').textContent = m.message;
    $('chapterNote').textContent = m.caption || '';
    setImage($('chapterImg'), i);

    $('progressText').textContent = 'Your journey — ' + pad(i + 1) + ' of ' + pad(TOTAL);
    $('progressBar').style.width = ((i + 1) / TOTAL) * 100 + '%';

    $('prevBtn').disabled = i === 0;
    const last = i === TOTAL - 1;
    $('nextBtn').querySelector('.lbl').textContent = last ? 'All memories' : 'Next';
    $('nextBtn').setAttribute('aria-label', last ? 'See all memories' : 'Next memory');

    preload(i - 1);
    preload(i + 1);
  }

  function goToChapter(target, dir) {
    if (chapterBusy || target < 0 || target >= TOTAL) return;
    chapterBusy = true;
    const box = $('chapterContent');
    box.style.setProperty('--dx', dir * 28 + 'px');
    box.classList.add('is-out');
    setTimeout(() => {
      currentChapter = target;
      fillChapter(target);
      $('chapter').scrollTop = 0;
      box.classList.remove('is-out');
      box.classList.add('is-in');
      setTimeout(() => { box.classList.remove('is-in'); chapterBusy = false; }, T(800));
    }, T(240));
  }

  function nextChapter(e) {
    if (e && e.clientX) burst(e.clientX, e.clientY, 4);
    if (currentChapter === TOTAL - 1) showScreen('overview');
    else goToChapter(currentChapter + 1, 1);
  }
  function prevChapter() { goToChapter(currentChapter - 1, -1); }

  /* =====================================================
     GALLERY
     ===================================================== */
  function buildGallery() {
    const grid = $('galleryGrid');
    grid.innerHTML = '';
    memories.forEach((m, i) => {
      const li = document.createElement('li');
      li.className = 'snap-item';
      li.style.setProperty('--n', i);

      const b = document.createElement('button');
      b.type = 'button';
      b.className = 'snap';
      b.dataset.frame = FRAMES[i % FRAMES.length];
      b.setAttribute('aria-label', 'Open memory ' + (i + 1) + ': ' + m.title + ', ' + m.date);
      b.innerHTML =
        '<span class="snap-photo"><img alt=""></span>' +
        '<span class="snap-cap"><span class="snap-no"></span><span class="snap-title"></span><span class="snap-date"></span></span>';
      b.querySelector('.snap-no').textContent = 'No. ' + pad(i + 1);
      b.querySelector('.snap-title').textContent = m.title;
      b.querySelector('.snap-date').textContent = m.date;
      const img = b.querySelector('img');
      setImage(img, i);
      img.alt = '';
      b.addEventListener('click', (e) => {
        if (e.clientX) burst(e.clientX, e.clientY, 4);
        openViewer(i, b);
      });
      li.appendChild(b);
      grid.appendChild(li);
    });
  }

  /* =====================================================
     MEMORY VIEWER
     ===================================================== */
  function fillViewer(i, animate) {
    const m = memories[i];
    viewerIndex = i;
    $('viewerChapter').textContent = 'Chapter ' + pad(i + 1) + ' / ' + pad(TOTAL);
    $('viewerTitle').textContent = m.title;
    $('viewerDate').textContent = m.date;
    $('viewerStory').textContent = m.story;
    $('viewerMessage').textContent = m.message;
    setImage($('viewerImg'), i);

    const body = $('viewerBody');
    body.scrollTop = 0;
    if (animate) {
      body.classList.remove('swap');
      void body.offsetWidth;
      body.classList.add('swap');
    }
    preload(i - 1);
    preload(i + 1);
  }

  function openViewer(i, trigger) {
    lastFocus = trigger || document.activeElement;
    fillViewer(i, false);
    const v = $('viewer');
    v.classList.add('open');
    v.setAttribute('aria-hidden', 'false');
    setTimeout(() => $('viewerClose').focus({ preventScroll: true }), 60);
  }
  function viewerIsOpen() { return $('viewer').classList.contains('open'); }
  function closeViewer() {
    if (!viewerIsOpen()) return;
    const v = $('viewer');
    v.classList.remove('open');
    v.setAttribute('aria-hidden', 'true');
    if (lastFocus && lastFocus.focus) lastFocus.focus({ preventScroll: true });
  }
  function stepViewer(dir, e) {
    if (e && e.clientX) burst(e.clientX, e.clientY, 3);
    fillViewer((viewerIndex + dir + TOTAL) % TOTAL, true);
  }

  /* =====================================================
     LOVE LETTER
     ===================================================== */
  function buildLetter() {
    const box = $('letterText');
    box.innerHTML = '';
    loveLetter.forEach((line, i) => {
      const p = document.createElement('p');
      p.textContent = line;
      if (i === 0) p.className = 'salutation';
      if (i === loveLetter.length - 1) p.className = 'signature';
      box.appendChild(p);
    });
  }

  function openEnvelope() {
    if (letterOpened) return;
    letterOpened = true;
    const env = $('envelope');
    env.classList.add('open');                               // flap opens, card rises
    $('letterHint').style.opacity = '0';
    $('letterLabel').style.opacity = '0';
    burstFrom(env, 6);

    setTimeout(() => env.classList.add('leaving'), T(1800));
    setTimeout(() => {
      env.hidden = true;
      $('letterHint').hidden = true;
      $('letterLabel').hidden = true;
      const sheet = $('letterPaper');
      const paras = sheet.querySelectorAll('.letter-text p');
      paras.forEach((p, i) => p.style.setProperty('--d', (T(500) + i * T(480)) / 1000 + 's'));
      sheet.classList.add('shown');
      $('letter').scrollTop = 0;
      sheet.focus({ preventScroll: true });
      setTimeout(() => $('replayBtn').classList.add('show'), T(500) + paras.length * T(480) + T(700));
    }, T(2400));
  }

  function resetLetter() {
    letterOpened = false;
    const env = $('envelope');
    env.hidden = false;
    env.classList.remove('open', 'leaving');
    $('letterHint').hidden = false;
    $('letterLabel').hidden = false;
    $('letterHint').style.opacity = '';
    $('letterLabel').style.opacity = '';
    $('letterPaper').classList.remove('shown');
    $('replayBtn').classList.remove('show');
  }

  /* =====================================================
     REPLAY
     ===================================================== */
  function replay() {
    if (journeyStarted) return;
    journeyStarted = true;
    closeViewer();
    heartTransition(() => {
      resetLetter();
      currentChapter = 0;
      chapterBusy = false;
      $('chapterContent').classList.remove('is-out', 'is-in');
      fillChapter(0);
      showScreen('opening');
    }, () => { journeyStarted = false; });
  }

  /* =====================================================
     INPUT HELPERS
     ===================================================== */
  function addSwipe(el, onLeft, onRight) {
    let x0 = 0, y0 = 0, on = false;
    el.addEventListener('touchstart', (e) => {
      if (e.touches.length !== 1) return;
      x0 = e.touches[0].clientX; y0 = e.touches[0].clientY; on = true;
    }, { passive: true });
    el.addEventListener('touchend', (e) => {
      if (!on) return;
      on = false;
      const c = e.changedTouches[0];
      const dx = c.clientX - x0, dy = c.clientY - y0;
      if (Math.abs(dx) > 60 && Math.abs(dx) > Math.abs(dy) * 1.6) (dx < 0 ? onLeft : onRight)();
    }, { passive: true });
  }

  function trapFocus(e) {
    const f = Array.from($('viewer').querySelectorAll('button:not([disabled])'));
    if (!f.length) return;
    const first = f[0], last = f[f.length - 1];
    if (e.shiftKey && document.activeElement === first) { e.preventDefault(); last.focus(); }
    else if (!e.shiftKey && document.activeElement === last) { e.preventDefault(); first.focus(); }
  }

  /* =====================================================
     START EVERYTHING
     ===================================================== */
  function init() {
    buildAtmosphere();
    buildGallery();
    buildLetter();
    setupMusic();
    setupLock();
    fillChapter(0);
    renderPin();

    document.querySelectorAll('[data-memory]').forEach((img) => {
      setImage(img, +img.dataset.memory);
      img.alt = '';
    });
    document.querySelectorAll('.screen').forEach((s) => {
      s.setAttribute('tabindex', '-1');
      s.setAttribute('aria-hidden', s.classList.contains('active') ? 'false' : 'true');
    });

    $('beginBtn').addEventListener('click', beginJourney);
    $('prevBtn').addEventListener('click', prevChapter);
    $('nextBtn').addEventListener('click', nextChapter);

    $('toLetterBtn').addEventListener('click', (e) => {
      if (e.clientX) burst(e.clientX, e.clientY, 5);
      resetLetter();
      showScreen('letter');
    });

    $('viewerClose').addEventListener('click', closeViewer);
    $('viewerBack').addEventListener('click', closeViewer);
    $('viewerBackdrop').addEventListener('click', closeViewer);
    $('viewerPrev').addEventListener('click', (e) => stepViewer(-1, e));
    $('viewerNext').addEventListener('click', (e) => stepViewer(1, e));

    const env = $('envelope');
    env.addEventListener('click', openEnvelope);
    env.addEventListener('keydown', (e) => {
      if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); openEnvelope(); }
    });
    $('replayBtn').addEventListener('click', replay);

    addSwipe($('chapter'),
      () => { if (currentChapter < TOTAL - 1) goToChapter(currentChapter + 1, 1); },
      () => prevChapter());
    addSwipe($('viewerBody'), () => stepViewer(1), () => stepViewer(-1));

    document.addEventListener('keydown', (e) => {
      if (viewerIsOpen()) {
        if (e.key === 'Escape') closeViewer();
        else if (e.key === 'ArrowRight') stepViewer(1);
        else if (e.key === 'ArrowLeft') stepViewer(-1);
        else if (e.key === 'Tab') trapFocus(e);
        return;
      }
      if ($('chapter').classList.contains('active')) {
        if (e.key === 'ArrowRight') nextChapter(e);
        else if (e.key === 'ArrowLeft') prevChapter();
      }
    });
  }

  if (document.readyState === 'loading') document.addEventListener('DOMContentLoaded', init);
  else init();
})();
