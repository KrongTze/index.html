import React, { useState, useEffect } from 'react';
import { Play, RotateCcw, Zap } from 'lucide-react';

export default function BlockchainSpeedDemo() {
  const [isRacing, setIsRacing] = useState(false);
  const [progress, setProgress] = useState({});
  const [finished, setFinished] = useState([]);
  const [autoRepeat, setAutoRepeat] = useState(false);

  const blockchains = [
    { 
      name: 'MultiversX Supernova', 
      finality: 250, 
      color: '#00D4AA',
      glow: 'rgba(0, 212, 170, 0.5)',
      label: '250ms Instant Finality'
    },
    { 
      name: 'Sui', 
      finality: 400, 
      color: '#6FBCF0',
      glow: 'rgba(111, 188, 240, 0.4)',
      label: '~400ms Checkpoint'
    },
    { 
      name: 'Solana', 
      finality: 2500, 
      color: '#14F195',
      glow: 'rgba(20, 241, 149, 0.4)',
      label: '~2.5s Probabilistic'
    },
    { 
      name: 'Aptos', 
      finality: 2000, 
      color: '#00E5C8',
      glow: 'rgba(0, 229, 200, 0.4)',
      label: '~2s BFT'
    },
    { 
      name: 'Avalanche', 
      finality: 1500, 
      color: '#E84142',
      glow: 'rgba(232, 65, 66, 0.4)',
      label: '~1.5s Instant'
    },
    { 
      name: 'Near', 
      finality: 1500, 
      color: '#00C1DE',
      glow: 'rgba(0, 193, 222, 0.4)',
      label: '~1.5s BFT'
    },
    { 
      name: 'BNB Chain', 
      finality: 3000, 
      color: '#F3BA2F',
      glow: 'rgba(243, 186, 47, 0.4)',
      label: '~3s Probabilistic'
    },
  ];

  const maxFinality = Math.max(...blockchains.map(b => b.finality));

  const startRace = () => {
    setIsRacing(true);
    setProgress({});
    setFinished([]);

    // Animate each blockchain independently
    blockchains.forEach((blockchain) => {
      const startTime = Date.now();
      const duration = blockchain.finality;

      const animate = () => {
        const elapsed = Date.now() - startTime;
        const currentProgress = Math.min((elapsed / duration) * 100, 100);
        
        setProgress(prev => ({
          ...prev,
          [blockchain.name]: currentProgress
        }));

        if (currentProgress < 100) {
          requestAnimationFrame(animate);
        } else {
          setFinished(prev => [...prev, blockchain.name]);
        }
      };

      requestAnimationFrame(animate);
    });

    // End race when slowest finishes
    setTimeout(() => {
      setIsRacing(false);
    }, maxFinality + 500);
  };

  const reset = () => {
    setIsRacing(false);
    setProgress({});
    setFinished([]);
  };

  const toggleAutoRepeat = () => {
    setAutoRepeat(!autoRepeat);
    if (!autoRepeat && !isRacing) {
      startRace();
    }
  };

  // Auto-repeat effect
  useEffect(() => {
    if (autoRepeat && !isRacing && Object.keys(progress).length > 0) {
      const allFinished = finished.length === blockchains.length;
      if (allFinished) {
        const timer = setTimeout(() => {
          reset();
          setTimeout(() => startRace(), 100);
        }, 2000);
        
        return () => clearTimeout(timer);
      }
    }
  }, [autoRepeat, isRacing, finished, progress]);

  // Start automatically on mount if autoRepeat is enabled
  useEffect(() => {
    if (autoRepeat) {
      startRace();
    }
  }, []);

  const getProgress = (blockchain) => {
    return progress[blockchain.name] || 0;
  };

  const getPosition = (name) => {
    if (!finished.includes(name)) return null;
    
    // Sort finished blockchains by their finality time
    const sortedFinished = finished
      .map(fname => blockchains.find(b => b.name === fname))
      .sort((a, b) => a.finality - b.finality);
    
    return sortedFinished.findIndex(b => b.name === name) + 1;
  };

  return (
    <div style={{
      minHeight: '100vh',
      background: 'linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f1628 100%)',
      padding: '40px 20px',
      fontFamily: '"SF Mono", "Courier New", monospace',
      position: 'relative',
      overflow: 'hidden'
    }}>
      {/* Animated background grid */}
      <div style={{
        position: 'absolute',
        inset: 0,
        backgroundImage: `
          linear-gradient(rgba(0, 212, 170, 0.03) 1px, transparent 1px),
          linear-gradient(90deg, rgba(0, 212, 170, 0.03) 1px, transparent 1px)
        `,
        backgroundSize: '50px 50px',
        animation: 'gridPulse 4s ease-in-out infinite'
      }} />

      <style>{`
        @keyframes gridPulse {
          0%, 100% { opacity: 0.3; }
          50% { opacity: 0.6; }
        }
        
        @keyframes slideIn {
          from {
            transform: translateX(-100%);
          }
          to {
            transform: translateX(0);
          }
        }
        
        @keyframes glow {
          0%, 100% { 
            box-shadow: 0 0 20px currentColor, 0 0 40px currentColor;
          }
          50% { 
            box-shadow: 0 0 30px currentColor, 0 0 60px currentColor;
          }
        }

        @keyframes trophy {
          0%, 100% { transform: translateY(0) rotate(0deg); }
          50% { transform: translateY(-5px) rotate(5deg); }
        }

        .winner-badge {
          animation: trophy 0.6s ease-in-out infinite;
        }
      `}</style>

      <div style={{ maxWidth: '1400px', margin: '0 auto', position: 'relative', zIndex: 1 }}>
        {/* Header */}
        <div style={{ textAlign: 'center', marginBottom: '60px' }}>
          <div style={{
            display: 'inline-flex',
            alignItems: 'center',
            gap: '12px',
            marginBottom: '20px',
            padding: '8px 20px',
            background: 'rgba(0, 212, 170, 0.1)',
            borderRadius: '50px',
            border: '1px solid rgba(0, 212, 170, 0.3)'
          }}>
            <Zap size={20} color="#00D4AA" />
            <span style={{ color: '#00D4AA', fontSize: '14px', fontWeight: '600' }}>
              LIVE DEMO
            </span>
          </div>
          
          <h1 style={{
            fontSize: '56px',
            fontWeight: '700',
            margin: '0 0 16px 0',
            background: 'linear-gradient(135deg, #00D4AA 0%, #00E5FF 100%)',
            WebkitBackgroundClip: 'text',
            WebkitTextFillColor: 'transparent',
            letterSpacing: '-2px'
          }}>
            Blockchain Finality Race
          </h1>
          
          <p style={{
            color: 'rgba(255, 255, 255, 0.6)',
            fontSize: '18px',
            maxWidth: '600px',
            margin: '0 auto',
            lineHeight: '1.6'
          }}>
            Watch transactions reach <strong style={{ color: '#00D4AA' }}>instant finality</strong> across different blockchains. 
            First to finish = fastest settlement.
          </p>
        </div>

        {/* Control buttons */}
        <div style={{
          display: 'flex',
          justifyContent: 'center',
          gap: '16px',
          marginBottom: '50px',
          flexWrap: 'wrap'
        }}>
          <button
            onClick={toggleAutoRepeat}
            style={{
              display: 'flex',
              alignItems: 'center',
              gap: '10px',
              padding: '16px 32px',
              fontSize: '16px',
              fontWeight: '600',
              color: autoRepeat ? '#0a0e27' : 'rgba(255, 255, 255, 0.9)',
              background: autoRepeat ? '#00D4AA' : 'rgba(255, 255, 255, 0.1)',
              border: autoRepeat ? 'none' : '1px solid rgba(255, 255, 255, 0.2)',
              borderRadius: '12px',
              cursor: 'pointer',
              transition: 'all 0.3s ease',
              fontFamily: 'inherit',
              boxShadow: autoRepeat ? '0 4px 20px rgba(0, 212, 170, 0.4)' : 'none'
            }}
          >
            <Play size={20} />
            {autoRepeat ? '🔄 Auto-Repeat ON' : 'Enable Auto-Repeat'}
          </button>

          <button
            onClick={startRace}
            disabled={isRacing || autoRepeat}
            style={{
              display: 'flex',
              alignItems: 'center',
              gap: '10px',
              padding: '16px 32px',
              fontSize: '16px',
              fontWeight: '600',
              color: (isRacing || autoRepeat) ? 'rgba(255, 255, 255, 0.4)' : '#fff',
              background: (isRacing || autoRepeat) ? 'rgba(255, 255, 255, 0.1)' : 'rgba(255, 255, 255, 0.15)',
              border: '1px solid rgba(255, 255, 255, 0.2)',
              borderRadius: '12px',
              cursor: (isRacing || autoRepeat) ? 'not-allowed' : 'pointer',
              transition: 'all 0.3s ease',
              fontFamily: 'inherit',
              opacity: (isRacing || autoRepeat) ? 0.5 : 1
            }}
          >
            <Play size={20} />
            {isRacing ? 'Racing...' : 'Start Once'}
          </button>

          <button
            onClick={reset}
            disabled={isRacing || autoRepeat}
            style={{
              display: 'flex',
              alignItems: 'center',
              gap: '10px',
              padding: '16px 32px',
              fontSize: '16px',
              fontWeight: '600',
              color: 'rgba(255, 255, 255, 0.9)',
              background: 'rgba(255, 255, 255, 0.1)',
              border: '1px solid rgba(255, 255, 255, 0.2)',
              borderRadius: '12px',
              cursor: (isRacing || autoRepeat) ? 'not-allowed' : 'pointer',
              transition: 'all 0.3s ease',
              fontFamily: 'inherit',
              opacity: (isRacing || autoRepeat) ? 0.5 : 1
            }}
          >
            <RotateCcw size={20} />
            Reset
          </button>
        </div>

        {/* Race tracks */}
        <div style={{
          display: 'flex',
          flexDirection: 'column',
          gap: '24px',
          background: 'rgba(0, 0, 0, 0.3)',
          padding: '40px',
          borderRadius: '24px',
          border: '1px solid rgba(255, 255, 255, 0.1)',
          backdropFilter: 'blur(10px)'
        }}>
          {blockchains.map((blockchain, index) => {
            const currentProgress = getProgress(blockchain);
            const position = getPosition(blockchain.name);
            const isFinished = finished.includes(blockchain.name);

            return (
              <div key={blockchain.name} style={{
                position: 'relative'
              }}>
                {/* Blockchain info */}
                <div style={{
                  display: 'flex',
                  justifyContent: 'space-between',
                  alignItems: 'center',
                  marginBottom: '12px'
                }}>
                  <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
                    <span style={{
                      fontSize: '16px',
                      fontWeight: '700',
                      color: blockchain.color,
                      minWidth: '200px'
                    }}>
                      {blockchain.name}
                    </span>
                    
                    {isFinished && position && position <= 3 && (
                      <span className="winner-badge" style={{
                        fontSize: '20px',
                        filter: `drop-shadow(0 0 8px ${blockchain.color})`
                      }}>
                        {position === 1 ? '🏆' : position === 2 ? '🥈' : '🥉'}
                      </span>
                    )}
                  </div>

                  <span style={{
                    fontSize: '13px',
                    color: 'rgba(255, 255, 255, 0.5)',
                    fontWeight: '500'
                  }}>
                    {blockchain.label}
                  </span>
                </div>

                {/* Track */}
                <div style={{
                  height: '48px',
                  background: 'rgba(255, 255, 255, 0.05)',
                  borderRadius: '12px',
                  position: 'relative',
                  overflow: 'hidden',
                  border: '1px solid rgba(255, 255, 255, 0.1)'
                }}>
                  {/* Progress bar */}
                  <div style={{
                    position: 'absolute',
                    left: 0,
                    top: 0,
                    height: '100%',
                    width: `${currentProgress}%`,
                    background: `linear-gradient(90deg, ${blockchain.color}, ${blockchain.glow})`,
                    transition: 'none',
                    boxShadow: isFinished ? `0 0 20px ${blockchain.glow}` : 'none'
                  }} />

                  {/* Transaction icon */}
                  {currentProgress > 0 ? (
                    <div style={{
                      position: 'absolute',
                      left: `calc(${currentProgress}% - 20px)`,
                      top: '50%',
                      transform: 'translateY(-50%)',
                      width: '32px',
                      height: '32px',
                      background: blockchain.color,
                      borderRadius: '8px',
                      display: 'flex',
                      alignItems: 'center',
                      justifyContent: 'center',
                      fontSize: '16px',
                      transition: 'none',
                      boxShadow: `0 0 20px ${blockchain.glow}`,
                      animation: isFinished ? 'glow 1s ease-in-out infinite' : 'none'
                    }}>
                      ⚡
                    </div>
                  ) : null}

                  {/* Finish line */}
                  <div style={{
                    position: 'absolute',
                    right: 0,
                    top: 0,
                    bottom: 0,
                    width: '3px',
                    background: 'rgba(255, 255, 255, 0.3)',
                    boxShadow: '0 0 10px rgba(255, 255, 255, 0.2)'
                  }} />
                </div>

                {/* Finish time */}
                {isFinished && position && (
                  <div style={{
                    position: 'absolute',
                    right: '10px',
                    bottom: '-2px',
                    fontSize: '12px',
                    fontWeight: '700',
                    color: blockchain.color,
                    background: 'rgba(0, 0, 0, 0.8)',
                    padding: '4px 10px',
                    borderRadius: '6px',
                    border: `1px solid ${blockchain.color}`
                  }}>
                    #{position} • {blockchain.finality}ms
                  </div>
                )}
              </div>
            );
          })}
        </div>

        {/* Results summary */}
        {finished.length === blockchains.length && !isRacing && (
          <div style={{
            marginTop: '40px',
            padding: '30px',
            background: 'rgba(0, 212, 170, 0.1)',
            border: '2px solid rgba(0, 212, 170, 0.3)',
            borderRadius: '20px',
            textAlign: 'center'
          }}>
            <div style={{
              fontSize: '24px',
              fontWeight: '700',
              color: '#00D4AA',
              marginBottom: '12px'
            }}>
              🏆 MultiversX Supernova Wins!
            </div>
            <div style={{
              fontSize: '16px',
              color: 'rgba(255, 255, 255, 0.7)',
              lineHeight: '1.6'
            }}>
              <strong style={{ color: '#fff' }}>250ms instant finality</strong> — 
              {' '}transactions permanently settled in a quarter second.
              <br />
              <span style={{ fontSize: '14px', opacity: 0.8 }}>
                That's <strong style={{ color: '#fff' }}>10× faster</strong> than Solana and <strong style={{ color: '#fff' }}>6× faster</strong> than Aptos.
              </span>
            </div>
          </div>
        )}

        {/* Info footer */}
        <div style={{
          marginTop: '50px',
          padding: '24px',
          background: 'rgba(255, 255, 255, 0.03)',
          borderRadius: '16px',
          border: '1px solid rgba(255, 255, 255, 0.1)'
        }}>
          <div style={{
            fontSize: '13px',
            color: 'rgba(255, 255, 255, 0.5)',
            lineHeight: '1.8',
            textAlign: 'center'
          }}>
            <strong style={{ color: 'rgba(255, 255, 255, 0.7)' }}>What is Finality?</strong>
            <br />
            Finality is when a transaction becomes irreversible and permanently settled on the blockchain.
            <br />
            Instant finality means <strong style={{ color: '#00D4AA' }}>zero reorganization risk</strong> — 
            perfect for payments, DEX trades, and cross-chain bridges.
          </div>
        </div>
      </div>
    </div>
  );
}
