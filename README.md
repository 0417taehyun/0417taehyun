<style>
    .termynal-comment {
        color: #4a968f;
        font-style: italic;
        display: block;
    }
  
    .termy [data-termynal] {
        white-space: pre-wrap;
    }

    /**
    * termynal.js
    *
    * @author Ines Montani <ines@ines.io>
    * @version 0.0.1
    * @license MIT
    */

    :root {
        --color-bg: #252a33;
        --color-text: #eee;
        --color-text-subtle: #a2a2a2;
    }

    [data-termynal] {
        width: 750px;
        max-width: 100%;
        background: var(--color-bg);
        color: var(--color-text);
        /* font-size: 18px; */
        font-size: 15px;
        /* font-family: 'Fira Mono', Consolas, Menlo, Monaco, 'Courier New', Courier, monospace; */
        font-family: 'Roboto Mono', 'Fira Mono', Consolas, Menlo, Monaco, 'Courier New', Courier, monospace;
        border-radius: 4px;
        padding: 75px 45px 35px;
        position: relative;
        -webkit-box-sizing: border-box;
                box-sizing: border-box;
    }

    [data-termynal]:before {
        content: '';
        position: absolute;
        top: 15px;
        left: 15px;
        display: inline-block;
        width: 15px;
        height: 15px;
        border-radius: 50%;
        /* A little hack to display the window buttons in one pseudo element. */
        background: #d9515d;
        -webkit-box-shadow: 25px 0 0 #f4c025, 50px 0 0 #3ec930;
                box-shadow: 25px 0 0 #f4c025, 50px 0 0 #3ec930;
    }

    [data-termynal]:after {
        content: 'bash';
        position: absolute;
        color: var(--color-text-subtle);
        top: 5px;
        left: 0;
        width: 100%;
        text-align: center;
    }

    a[data-terminal-control] {
        text-align: right;
        display: block;
        color: #aebbff;
    }

    [data-ty] {
        display: block;
        line-height: 2;
    }

    [data-ty]:before {
        /* Set up defaults and ensure empty lines are displayed. */
        content: '';
        display: inline-block;
        vertical-align: middle;
    }

    [data-ty="input"]:before,
    [data-ty-prompt]:before {
        margin-right: 0.75em;
        color: var(--color-text-subtle);
    }

    [data-ty="input"]:before {
        content: '$';
    }

    [data-ty][data-ty-prompt]:before {
        content: attr(data-ty-prompt);
    }

    [data-ty-cursor]:after {
        content: attr(data-ty-cursor);
        font-family: monospace;
        margin-left: 0.5em;
        -webkit-animation: blink 1s infinite;
                animation: blink 1s infinite;
    }


    /* Cursor animation */

    @-webkit-keyframes blink {
        50% {
            opacity: 0;
        }
    }

    @keyframes blink {
        50% {
            opacity: 0;
        }
    }    
</style>


<div class="termy">
    ```sh
    $ pip install weekwith.me
    ```
</div>