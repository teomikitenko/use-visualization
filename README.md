# use-visualization

Simple visualization for your audio/video`

## Installing

npm i use-visualization@latest

## Example

```javascript
import { useVisualization } from "use-visualization";
import { useRef } from "react";

const Audio = () => {
  const sourceRef = useRef < HTMLAudioElement > null;
  const canvasRef = useRef < HTMLCanvasElement > null;
  const { audioContext, onPlay, onPause } = useVisualization(
    sourceRef.current,
    canvasRef.current,
    "orange"
  );

  return (
    <div className="bg-red-300 w-full min-h-screen  px-6 pb-6 pt-14">
      <audio
        ref={sourceRef}
        src="/src/sample.mp3"
        controls
        onPlay={onPlay}
        onPause={onPause}
      />

      <canvas ref={canvasRef} className=" h-56 w-full" />
    </div>
  );
};

export default Audio;
```
