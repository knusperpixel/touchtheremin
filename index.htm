<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no" />
	<meta name="apple-mobile-web-app-capable" content="yes" />
	<meta name="apple-mobile-web-app-status-bar-style" content="black" />
	
	<title>TouchTheremin</title>
	
	<style type="text/css">
	html, body { height:100%; min-height:416px; box-sizing:border-box; }
	body {
		background:#FFF;
		color:#000;
		font:normal 12px sans-serif;
		margin:0;
		padding:20px;
	}
	#error {
		margin:0;
		padding:5px;
		background:#FCC;
		font-weight:bold;
	}
	#canvas {
		width:100%;
		height:100%;
		background:#333;
		-webkit-touch-callout: none;
		-webkit-user-select: none;
		color:#FFF;
	}
	</style>
	
	<script type="text/javascript">
	
	(function(win) {
		
		
		var context,
		 	sineWave,
			gainNode,
			doc = win.document, 
			$ = function(id) { return doc.getElementById(id) },
			canvas, canvasHeight, canvasWidth, canvasOffsetTop, canvasOffsetLeft;
		
		var calculateLevel = function(e) {
			
			var touch = e.touches[0], 
				y = touch.pageY - canvasOffsetTop,
				percent = 0;
			
			if(y < 0) { y = 0; }
			else if (y > canvasHeight) { y = canvasHeight; }
			
			percent = (y / canvasHeight);
			gainNode.gain.value = percent;
			
		};
		
		var calculateFrequency = function(e) {
			
			var touch = e.touches[0], 
				x = touch.pageX - canvasOffsetLeft,
				percent = 0;
			
			if(x < 0) { x = 0; }
			else if(x > canvasWidth) { x = canvasWidth; }
			
			percent = x / canvasWidth;
			sineWave.frequency.value = 2000 * percent;
			
		};
		
		win.addEventListener('DOMContentLoaded', function() {
			
			doc.ontouchmove = function(e) {
				e.preventDefault();
			};
			
			try {
				
				context = new webkitAudioContext();
				
				gainNode = context.createGainNode();
				gainNode.connect(context.destination);
				
				doc.getElementsByTagName('body')[0].innerHTML = '<div id="canvas"></div>';
				
				canvas = $('canvas');
				canvasHeight = canvas.clientHeight;
				canvasWidth = canvas.clientWidth;
				canvasOffsetTop = canvas.offsetTop;
				canvasOffsetLeft = canvas.offsetLeft;
				
				canvas.ontouchstart = function(e) {
					sineWave = context.createOscillator();
					sineWave.connect(gainNode);
					sineWave.noteOn(0);
					
					calculateLevel(e);
					calculateFrequency(e);
					
				};
				canvas.ontouchend = function(e) {
					sineWave.disconnect()
				};
				canvas.ontouchmove = function(e) {
					calculateLevel(e);
					calculateFrequency(e);
				};
				
			} catch (e) {
				
				$('error').innerHTML = 'Could not create AudioContext.';
				return;
				
			}
			
		});
		
	})(window);
	
	</script>
</head>
<body>
	<p id="error">Your browser is uncapable of running this page. Try Google Chrome or Safari.</p>
</body>
</html>