```aura width=800 height=220
<div style={{
  display: 'flex',
  flexDirection: 'column',
  alignItems: 'center',
  justifyContent: 'center',
  width: '100%',
  height: '100%',
  background: 'linear-gradient(160deg, #05050a 0%, #0d1120 50%, #141b30 100%)',
  borderRadius: '18px',
  border: '1px solid #232c47',
  gap: '18px',
  position: 'relative',
  overflow: 'hidden',
}}>
  <div style={{
    display: 'flex',
    position: 'absolute',
    top: '0',
    left: '0',
    right: '0',
    height: '3px',
    background: 'linear-gradient(90deg, #05050a 0%, #1c2540 30%, #3f8fe0 65%, #fbdfb8 100%)',
  }} />

  <svg width="800" height="220" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="moonglow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(63,143,224,0.16)" />
        <stop offset="60%" stopColor="rgba(63,143,224,0.04)" />
        <stop offset="100%" stopColor="rgba(63,143,224,0)" />
      </radialGradient>
    </defs>
    <circle cx="140" cy="110" r="150" fill="url(#moonglow)" />
    {[
      [58,36,1.4,0.9],[96,150,1.1,0.7],[40,170,1.6,0.8],[130,52,1.2,0.6],
      [700,40,1.5,0.85],[740,120,1.1,0.6],[670,175,1.3,0.75],[755,70,1,0.5],
      [620,30,1.2,0.55],[540,190,1,0.5],[600,150,1.4,0.65],[480,25,1.1,0.5],
      [30,90,1,0.55],[770,150,1.2,0.6],
    ].map(([cx,cy,r,o],i) => (
      <circle key={i} cx={cx} cy={cy} r={r} fill="#fbdfb8" opacity={o} />
    ))}
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: '22px', position: 'relative' }}>
    <div style={{
      display: 'flex',
      width: '82px',
      height: '82px',
      borderRadius: '50%',
      background: 'linear-gradient(135deg, #fbdfb8, #3f8fe0, #0b0308)',
      alignItems: 'center',
      justifyContent: 'center',
    }}>
      <div style={{
        display: 'flex',
        width: '74px',
        height: '74px',
        borderRadius: '50%',
        overflow: 'hidden',
        border: '2px solid #0d1120',
      }}>
        <img src="./.github/assets/avatar.jpg" style={{ width: '74px', height: '74px' }} />
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: '5px' }}>
      <span style={{
        fontSize: '38px',
        fontWeight: '700',
        color: '#fbdfb8',
        letterSpacing: '-1px',
      }}>
        Younes Menfalouti
      </span>
      <span style={{
        fontSize: '14px',
        color: '#6fa8dc',
        fontWeight: '500',
        letterSpacing: '1.5px',
        textTransform: 'uppercase',
      }}>
        robotics · computer vision · android
      </span>
    </div>
  </div>

  <div style={{ display: 'flex', gap: '8px', position: 'relative' }}>
    {[
      { tag: 'python',     color: '#4ea8de', bg: 'rgba(78,168,222,0.12)' },
      { tag: 'kotlin',     color: '#a78bd6', bg: 'rgba(167,139,214,0.12)' },
      { tag: 'java',       color: '#e0975a', bg: 'rgba(224,151,90,0.12)' },
      { tag: 'javascript', color: '#e8c884', bg: 'rgba(232,200,132,0.12)' },
    ].map(({ tag, color, bg }) => (
      <div key={tag} style={{
        display: 'flex',
        padding: '4px 14px',
        borderRadius: '6px',
        background: bg,
        border: `1px solid ${color}`,
        color: color,
        fontSize: '12px',
        fontWeight: '700',
        letterSpacing: '0.8px',
        textTransform: 'uppercase',
      }}>
        {tag}
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=84 link="https://github.com/Yunsmn/dewey"
(() => {
  const name  = 'dewey';
  const about = 'Android app that reads your PDFs on-device, works out what each one is, and files it.';
  const event = 'RevenueCat Shipaton 2026';
  const langs = [
    { tag: 'kotlin', color: '#a78bd6', bg: 'rgba(167,139,214,0.12)' },
    { tag: 'python', color: '#4ea8de', bg: 'rgba(78,168,222,0.12)' },
  ];

  return (
    <div style={{
      display: 'flex',
      flexDirection: 'column',
      justifyContent: 'center',
      width: '100%',
      height: '100%',
      padding: '0 28px 0 30px',
      gap: '8px',
      background: '#0d1120',
      borderRadius: '12px',
      border: '1px solid #232c47',
      position: 'relative',
      overflow: 'hidden',
    }}>
      <div style={{
        display: 'flex',
        position: 'absolute',
        top: '0',
        bottom: '0',
        left: '0',
        width: '3px',
        background: langs[0].color,
      }} />

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
          <span style={{ fontSize: '19px', fontWeight: '700', color: '#fbdfb8', letterSpacing: '-0.3px' }}>
            {name}
          </span>
          <div style={{ display: 'flex', gap: '6px' }}>
            {langs.map(({ tag, color, bg }) => (
              <div key={tag} style={{
                display: 'flex',
                padding: '2px 10px',
                borderRadius: '6px',
                background: bg,
                border: `1px solid ${color}`,
                color: color,
                fontSize: '11px',
                fontWeight: '700',
                letterSpacing: '0.8px',
                textTransform: 'uppercase',
              }}>
                {tag}
              </div>
            ))}
          </div>
        </div>
        {event ? <span style={{ fontSize: '12px', color: '#5b6b94' }}>{event}</span> : null}
      </div>

      <span style={{ fontSize: '14px', color: '#a9b4d0' }}>
        {about}
      </span>
    </div>
  );
})()
```

```aura width=800 height=84 link="https://github.com/Yunsmn/mars-mission-planner"
(() => {
  const name  = 'MARVIN';
  const about = 'Offline Mars rover planner: IBM Granite proposes routes, NumPy physics vetoes the risky ones.';
  const event = 'IBM AI Builders Challenge';
  const langs = [
    { tag: 'python', color: '#4ea8de', bg: 'rgba(78,168,222,0.12)' },
    { tag: 'javascript', color: '#e8c884', bg: 'rgba(232,200,132,0.12)' },
  ];

  return (
    <div style={{
      display: 'flex',
      flexDirection: 'column',
      justifyContent: 'center',
      width: '100%',
      height: '100%',
      padding: '0 28px 0 30px',
      gap: '8px',
      background: '#0d1120',
      borderRadius: '12px',
      border: '1px solid #232c47',
      position: 'relative',
      overflow: 'hidden',
    }}>
      <div style={{
        display: 'flex',
        position: 'absolute',
        top: '0',
        bottom: '0',
        left: '0',
        width: '3px',
        background: langs[0].color,
      }} />

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
          <span style={{ fontSize: '19px', fontWeight: '700', color: '#fbdfb8', letterSpacing: '-0.3px' }}>
            {name}
          </span>
          <div style={{ display: 'flex', gap: '6px' }}>
            {langs.map(({ tag, color, bg }) => (
              <div key={tag} style={{
                display: 'flex',
                padding: '2px 10px',
                borderRadius: '6px',
                background: bg,
                border: `1px solid ${color}`,
                color: color,
                fontSize: '11px',
                fontWeight: '700',
                letterSpacing: '0.8px',
                textTransform: 'uppercase',
              }}>
                {tag}
              </div>
            ))}
          </div>
        </div>
        {event ? <span style={{ fontSize: '12px', color: '#5b6b94' }}>{event}</span> : null}
      </div>

      <span style={{ fontSize: '14px', color: '#a9b4d0' }}>
        {about}
      </span>
    </div>
  );
})()
```

```aura width=800 height=84 link="https://github.com/Yunsmn/VELMA"
(() => {
  const name  = 'VELMA';
  const about = 'SO-101 arm in MuJoCo: vision-guided pick-and-place to about 1 mm, drivable by an LLM over MCP.';
  const event = '';
  const langs = [
    { tag: 'python', color: '#4ea8de', bg: 'rgba(78,168,222,0.12)' },
  ];

  return (
    <div style={{
      display: 'flex',
      flexDirection: 'column',
      justifyContent: 'center',
      width: '100%',
      height: '100%',
      padding: '0 28px 0 30px',
      gap: '8px',
      background: '#0d1120',
      borderRadius: '12px',
      border: '1px solid #232c47',
      position: 'relative',
      overflow: 'hidden',
    }}>
      <div style={{
        display: 'flex',
        position: 'absolute',
        top: '0',
        bottom: '0',
        left: '0',
        width: '3px',
        background: langs[0].color,
      }} />

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
          <span style={{ fontSize: '19px', fontWeight: '700', color: '#fbdfb8', letterSpacing: '-0.3px' }}>
            {name}
          </span>
          <div style={{ display: 'flex', gap: '6px' }}>
            {langs.map(({ tag, color, bg }) => (
              <div key={tag} style={{
                display: 'flex',
                padding: '2px 10px',
                borderRadius: '6px',
                background: bg,
                border: `1px solid ${color}`,
                color: color,
                fontSize: '11px',
                fontWeight: '700',
                letterSpacing: '0.8px',
                textTransform: 'uppercase',
              }}>
                {tag}
              </div>
            ))}
          </div>
        </div>
        {event ? <span style={{ fontSize: '12px', color: '#5b6b94' }}>{event}</span> : null}
      </div>

      <span style={{ fontSize: '14px', color: '#a9b4d0' }}>
        {about}
      </span>
    </div>
  );
})()
```

```aura width=800 height=84 link="https://github.com/Yunsmn/MeshForge"
(() => {
  const name  = 'MeshForge';
  const about = 'Turns 2D CAD floor plans into a single 3D mesh using SAM, ControlNet, and Hunyuan3D.';
  const event = '';
  const langs = [
    { tag: 'python', color: '#4ea8de', bg: 'rgba(78,168,222,0.12)' },
  ];

  return (
    <div style={{
      display: 'flex',
      flexDirection: 'column',
      justifyContent: 'center',
      width: '100%',
      height: '100%',
      padding: '0 28px 0 30px',
      gap: '8px',
      background: '#0d1120',
      borderRadius: '12px',
      border: '1px solid #232c47',
      position: 'relative',
      overflow: 'hidden',
    }}>
      <div style={{
        display: 'flex',
        position: 'absolute',
        top: '0',
        bottom: '0',
        left: '0',
        width: '3px',
        background: langs[0].color,
      }} />

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
          <span style={{ fontSize: '19px', fontWeight: '700', color: '#fbdfb8', letterSpacing: '-0.3px' }}>
            {name}
          </span>
          <div style={{ display: 'flex', gap: '6px' }}>
            {langs.map(({ tag, color, bg }) => (
              <div key={tag} style={{
                display: 'flex',
                padding: '2px 10px',
                borderRadius: '6px',
                background: bg,
                border: `1px solid ${color}`,
                color: color,
                fontSize: '11px',
                fontWeight: '700',
                letterSpacing: '0.8px',
                textTransform: 'uppercase',
              }}>
                {tag}
              </div>
            ))}
          </div>
        </div>
        {event ? <span style={{ fontSize: '12px', color: '#5b6b94' }}>{event}</span> : null}
      </div>

      <span style={{ fontSize: '14px', color: '#a9b4d0' }}>
        {about}
      </span>
    </div>
  );
})()
```

```aura width=800 height=84 link="https://github.com/Yunsmn/CodeQuest"
(() => {
  const name  = 'CodeQuest';
  const about = '2D game that teaches coding: type commands to move your character and solve puzzles.';
  const event = '';
  const langs = [
    { tag: 'java', color: '#e0975a', bg: 'rgba(224,151,90,0.12)' },
  ];

  return (
    <div style={{
      display: 'flex',
      flexDirection: 'column',
      justifyContent: 'center',
      width: '100%',
      height: '100%',
      padding: '0 28px 0 30px',
      gap: '8px',
      background: '#0d1120',
      borderRadius: '12px',
      border: '1px solid #232c47',
      position: 'relative',
      overflow: 'hidden',
    }}>
      <div style={{
        display: 'flex',
        position: 'absolute',
        top: '0',
        bottom: '0',
        left: '0',
        width: '3px',
        background: langs[0].color,
      }} />

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
          <span style={{ fontSize: '19px', fontWeight: '700', color: '#fbdfb8', letterSpacing: '-0.3px' }}>
            {name}
          </span>
          <div style={{ display: 'flex', gap: '6px' }}>
            {langs.map(({ tag, color, bg }) => (
              <div key={tag} style={{
                display: 'flex',
                padding: '2px 10px',
                borderRadius: '6px',
                background: bg,
                border: `1px solid ${color}`,
                color: color,
                fontSize: '11px',
                fontWeight: '700',
                letterSpacing: '0.8px',
                textTransform: 'uppercase',
              }}>
                {tag}
              </div>
            ))}
          </div>
        </div>
        {event ? <span style={{ fontSize: '12px', color: '#5b6b94' }}>{event}</span> : null}
      </div>

      <span style={{ fontSize: '14px', color: '#a9b4d0' }}>
        {about}
      </span>
    </div>
  );
})()
```

[![GitHub Stats](https://ghstats.dev/api/card?username=Yunsmn&bg=0d1120&text=a9b4d0&title_color=fbdfb8&icon_color=4ea8de&border_color=232c47&hide=trend%2Cavg%2Cactive_day%2Cgrade%2Ccontributions%2Crepos%2Cfollowers&custom_title=Stats&border_radius=10)](https://github.com/Yunsmn)
