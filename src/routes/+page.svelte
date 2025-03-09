<script>
  import "../routes/index.scss";
  import { copy } from "svelte-copy";

  let copy_btn = document.querySelector(".copy");

  let change_text = (e) => {
    e.target.textContent = "Copied";
    setTimeout(() => {
      e.target.textContent = "Copy SCSS";
    }, 1500);
  };
</script>

<div class="mesh">
  <span class="made_in">Modern animations ⚡️ Made in 71428</span>
  <h1>
    <span class="wow_effect">WOW</span> your audience with
    <span>next-level <span class="wow_effect">SCSS</span> animations*</span>
  </h1>
  <p>
    Enhance your website with stunning SCSS animations that captivate visitors
    and create a smooth, modern, and engaging experience
  </p>

  <div class="animations">
    <div>
      <p>Button radius animation</p>
      <button>Hover me 💧</button>
      <button
        onclick={change_text}
        class="copy"
        use:copy={`
        button {
        width: 140px;
        padding: 10px 5px;
        background-color: transparent;
        color: white;
        border: 3px solid #6c3ee9;
        border-radius: 6px;
        cursor: pointer;
        transition: 0.3s;
        &:hover {
          background-color: #7145ec;
          border-radius: 50px;
        }
      }
      `}>Copy SCSS</button
      >
    </div>
    <div>
      <p>Move up animation</p>
      <div>
        <p>Hover me 🌌</p>
      </div>
      <button
        onclick={change_text}
        class="copy"
        use:copy={`
  div {
    width: 120px;
    height: 120px;
    background: linear-gradient(#6c3ee9, #310e88);
    display: grid;
    place-items: center;
    cursor: pointer;
    transition: 0.2s;
    border-radius: 10px;
    padding: 10px;
  &:hover {
      transform: translateY(-10px);
    }
  }`}>Copy SCSS</button
      >
    </div>
    <div>
      <p>Typewriter animation</p>
      <span>This is cool! SUPER COOL ☄️</span>
      <button
        onclick={change_text}
        class="copy"
        use:copy={`
            span {
        color: gray;
        overflow: hidden;
        border-right: 0.15em solid #7145ec;
        white-space: nowrap;
        margin: 0 auto;
        animation: typing 3.5s steps(40, end), blink_caret 1s step-end infinite;
      }
      @keyframes typing {
        from {
          width: 0;
        }
        to {
          width: 100%;
          max-width: max-content;
        }
      }

      @keyframes blink_caret {
        from,
        to {
          border-color: transparent;
        }
        50% {
          border-color: #7145ec;
        }
      }
      `}>Copy SCSS</button
      >
    </div>
    <div>
      <p>Shake animation</p>
      <div class="hover">Hover me 🌊</div>
      <button
        onclick={change_text}
        class="copy"
        use:copy={`
      div {
        width: 120px;
        height: 120px;
        background: linear-gradient(#6c3ee9, #310e88);
        display: grid;
        place-items: center;
        cursor: pointer;
        transition: 0.2s;
        border-radius: 10px;
        padding: 10px;
        color: white;
        &:hover {
          animation: shake_animation 1.5s infinite;
        }
      }
      @keyframes shake_animation {
        0% {
          transform: rotate(0deg);
        }
        80% {
          transform: rotate(0deg);
        }
        85% {
          transform: rotate(5deg);
        }
        95% {
          transform: rotate(-5deg);
        }
        100% {
          transform: rotate(0deg);
        }
      }
      `}>Copy SCSS</button
      >
    </div>
    <div>
      <h2>Stay tuned more animations are coming soon!</h2>
    </div>
  </div>
  <p class="tweak">Feel free to customize it to suit your needs! 😉</p>
</div>
