<script lang="ts">
    import fLogo from "../assets/F.svg";
    import fArmLogo from "../assets/F-arm.svg";
    import mLogo from "../assets/M.svg";
    export let size: string = "1";
</script>

<a href="/" target="_self" class="logobox" style="--logo-height:{`${size}vw`}">
    <div class="logo F">
        <img src={fLogo} alt="F Logo" />
        <div class="nameText">raser</div>
    </div>
    <div class="logo M">
        <img src={mLogo} alt="M Logo" />
        <div class="nameText">orrison</div>
    </div>
    <div class="logo FArm">
        <img src={fArmLogo} alt="F Logo" />
        <div class="nameText">r</div>
    </div>
</a>

<style lang="css">
    /**Grid Layout*/
    .logobox {
        display: grid;
        grid-template: 1 / 1;
        top: 0;
        width: calc(3 * var(--logo-height));
        padding-left: calc(1 * var(--logo-height));
        transition: width 1s ease-in-out;
    }
    .logobox > * {
        grid-column: 1/1;
        grid-row: 1/1;
    }
    .logobox:hover {
        width: calc(16 * var(--logo-height));
    }

    /**Animations*/
    .logobox:hover .nameText {
        transition: width 1s ease-in-out 0.5s;
        width: calc(6 * var(--logo-height));
    }
    .logobox:hover .M {
        transform: translate(calc(7 * var(--logo-height)), 0);
        transition: 1s ease-in-out;
    }
    .nameText {
        width: 0;
        transition: width 0.75s ease-in-out;
    }
    .M {
        transition: 1s ease-in-out;
    }

    /**Contents*/
    .logo {
        top: 0;
        left: 0;
        width: fit-content;
    }
    .logo.FArm {
        float: left;
        z-index: 1;
    }
    .logo img {
        height: calc(2 * var(--logo-height));
    }
    .logo.M {
        float: right;
    }
    .logo.F {
        float: left;
    }
    /**Put letters closer to F*/
    .logo.F img {
        margin-right: calc(-0.5 * var(--logo-height));
    }
    .logo.FArm img {
        margin-right: calc(-0.5 * var(--logo-height));
    }
    /**Text formatting*/
    .nameText {
        display: inline-flex;
        overflow: hidden;
        font-size: calc(2 * var(--logo-height));
        font-weight: 500;
        font-family: Arial, Helvetica, sans-serif;
        color: #646cff;
    }
    /* * {
        outline: black solid;
    } */
</style>
