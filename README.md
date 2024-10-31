# use-visualization

> Simple visualization for your audio/video

## Installing

`npm i use-visualization@latest`

## Example

```javascript
import { useVisualization } from "use-visualization";
import { useRef } from "react";

const Video = () => {
  const videoRef = useRef(null);
  const canvasRef = useRef(null);
  const color = "hsl(142.1 76.2% 36.3%)";

  useVisualization(videoRef.current, canvasRef.current, color);

  return (
    <div className="px-6 pb-6 pt-14">
      <video
        ref={videoRef}
        crossOrigin="anonymous"
        controls
        className="h-36 w-1/2"
        src="/src/sample.mp4"
      ></video>
      <canvas ref={canvasRef} className="h-56 w-full opacity-55 sm:bottom-20" />
    </div>
  );
};

export default Video;
```
