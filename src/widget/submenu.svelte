<script>
    import data from './submenu.json'
    import {page} from '$app/stores'
</script>

<div class='submenu'>
    <nav class='shadow-[inset_0_-1px_#EAEAEA]'>
        <div class='relative h-12 max-w-5xl m-auto overflow-hidden -mt-2.5'>
            <div class='ease-in duration-200'>
                <div class='flex items-end h-12 mx-auto my-auto -mt-px text-base font-medium leading-normal overflow-auto min-w-full z-10'>
                    <div class='flex items-center flex-grow-1 flex-shrink-0 '>
                        <div class='flex'>
                            <div class='highlight h-8 absolute bg-gray-50 left-0 -z-10 opacity-0 rounded '></div>
                            {#each data as item}
                                <a href={item.href} class:active={item.href === $page.url.pathname} class='tab relative text-gray-500 hover:text-gray-700 inline-block select-none cursor-pointer'>{item.label}</a>
                            {/each}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</div>

<style>
    .highlight {
        contain: strict;
        top: 9px;
        border-radius: 4px;
        z-index: -1;
        transition: .15s ease;
        transition-property: width,transform,opacity;
    }

    .tab {
        padding: 16px 12px;
        font-size: 14px;
        font-weight: 400;
        transition: color .2s ease;
    }
    
    .tab.active {
        color: #333;
    }
    .tab.active:before {
        content: '';
        display: block;
        position: absolute;
        height: 0;
        left: 9px;
        right: 9px;
        bottom: 0;
        border-bottom: 2px solid;
    }
</style>