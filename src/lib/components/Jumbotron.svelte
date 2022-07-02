<script>
    let image1 = "/images/img001.jpg"
    let image2 = "/images/img002.jpg"
    let image3  = "/images/img003.jpg"
    let image4  = "/images/img004.jpg"
    let video1 = "/videos/videos001.mp4"

    let position = 0
    let maxPostion = 400
    let minPosition = 0

    let playButton = true
    let pauseButton = false

    let counter = 1

    let description = true

    let duration;
    let time = 0
    let currentPercent = 0

    


    function handleNextButton(e) {
        counter++
        e.target.closest('section').querySelector('video').pause()
         playButton = true
         pauseButton = false
         description = true

        if (position == maxPostion) return
        position += 100
    }

    function handlePrevButton() {
        counter--
        if (position == minPosition) return
        position -= 100
    }

    function playVideo(e) {
        e.target.closest('.item').querySelector('video').play();
        playButton = false
        pauseButton = true
        description = false
    }

    function updateProgress(){
        currentPercent = (time / duration) * 100
    }

    function pauseVideo(e) {
        e.target.closest('.item').querySelector('video').pause();
        playButton = true
        pauseButton = false
        description = true
    }

    function handleEnd() {
        playButton = true
        pauseButton = false
        description = true
        currentPercent = 0
    }

</script>

<section>
   <div class="inner" style="transform: translateX(calc(-{position}% / 5));">
        <div class="item">
            <div class="overlay {description ? '' : 'hide'}" style="background-image: url({image4});"></div>
            <video
		    poster="{image4}"
		    src="{video1}"
            bind:duration="{duration}"
            bind:currentTime="{time}"
            on:timeupdate="{updateProgress}"
            on:ended={handleEnd}>
		    <track kind="captions">
	        </video>
            <div class="description {description ? '' : 'hide'}">
                <h1>Erin & Joses</h1>
                <p>Couple Session</p>
            </div>
            <div class="button">
                <div class="playButton {playButton ? '' : 'hide'}" on:click="{playVideo}"><i class="fa-solid fa-play fa-fade"></i></div>
                 <div class="pauseButton {pauseButton ? 'show' : ''}" on:click="{pauseVideo}"><i class="fa-solid fa-pause"></i></div>
            </div>
            <div class="progressBar"></div>
            <div class="progress" style="width: {currentPercent}%;"></div>
           
        </div>
        <div class="item" style="background-image: url({image1});"></div>
        <div class="item" style="background-image: url({image2});"></div>
        <div class="item" style="background-image: url({image3});"></div>
        <div class="item" style="background-image: url({image4});"></div>
   </div>
   <div class="prev {position == minPosition ? 'hide' : ''}" on:click="{handlePrevButton}"><i class="fa-solid fa-angle-left"></i></div>
   <div class="next {position == maxPostion ? 'hide' : ''}" on:click={handleNextButton}><i class="fa-solid fa-angle-right"></i></div>
   <div class="counter">{counter} / 5</div>
</section>


<style>
  section {
    height: 100vh;
    overflow: hidden;
    position: relative;
    color: var(--fn-white-color);
  }

  .inner {
   height: 100vh;
   width: 500vw;
   display: flex;
   justify-content: flex-start;
   align-items: center;
   transition: all 0.3s ease-in-out;
  }

  .item {
    height: 100vh;
    width: 100vw;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    
}

.overlay {
    position: absolute;
    top: 0;
    left: 0;
    background-color: black;
    height: 100%;
    width: 100%;
    transition: all 0.3s ease-in-out;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
}

.overlay.hide {
    opacity: 0;
}

.description {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    pointer-events: none;
    transition: all 0.4s ease-in-out;
    opacity: 1;
    text-transform: uppercase;
    
}

.description.hide {
    opacity: 0;
}

.description h1 {
    letter-spacing: 2px;
    font-size: 40px;
    font-weight: 100;
    
    
}

.description p {
    font-size: 13px;
    letter-spacing: 5px;

}


.button {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
}



.playButton {
    position: absolute;
    cursor: pointer;
    font-size: 1.3rem;
    background-color: rgba(0, 0, 0, 0.473);
    padding: 0.3rem 1rem;
    border-radius: 0.5rem;
    cursor: pointer;
    z-index: 999;
    opacity: 1;
    pointer-events: all;
    display: inline-block;
    bottom: 1rem;
    right: 2.5rem;
    transform: translate(-50%, -50%);
    transition: all 0.3s ease-in-out;
} 


.playButton.hide {
    opacity: 0;
   
}
.pauseButton {
    position: absolute;
    cursor: pointer;
    font-size: 1.3rem;
    background-color: rgba(0, 0, 0, 0.473);
    padding: 0.3rem 1rem;
    border-radius: 0.5rem;
    cursor: pointer;
    z-index: 999;
    opacity: 0;
    pointer-events: none;
    transition: all 0.3s ease-in-out;
    bottom: 1rem;
    right: 2.5rem;
    transform: translate(-50%, -50%);
} 

.pauseButton.show {
    opacity: 1;
    pointer-events: all;
   
}

video {
    width: 100%;
    object-fit: cover;
    height: 100%;
}

  .next {
    position: absolute;
    top: 50vh;
    right: 2rem;
    cursor: pointer;
  }

  .next.hide {
    display: none;
  }

  .prev {
    position: absolute;
    top: 50vh;
    left: 2rem;
    cursor: pointer;
  }

  .prev.hide {
    display: none;
  }

  .counter {
    position: absolute;
    bottom: 2.5rem;
    left: 2.5rem;
    font-size: 0.9em;
  }

  .progressBar {
    position: absolute;
    width: 100%;
    height: 5px;
    left: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.456);
  }

  .progress {
    position: absolute;
    height: 5px;
    left: 0;
    bottom: 0;
    background-color: #263405;
    transition: 0.3s ease-in-out;
    border-radius: 9999px;
  }
</style>