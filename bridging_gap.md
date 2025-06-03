---
layout: page
title: Bridging the knowledge gap
image: assets/images/pic07.JPG
nav-menu: true
---

<style>
    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        margin: 0;
        padding: 0;
        background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        min-height: 100vh;
    }
    
    .dashboard-container {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 80vh;
        padding: 40px 20px 20px 20px;
    }
    
    .dashboard-frame {
        width: 85%;
        background: white;
        border-radius: 12px;
        box-shadow: 0 8px 32px rgba(0,0,0,0.1);
        overflow: hidden;
    }
    
    /* Override Tableau sizing */
    .tableauViz {
        max-width: none !important;
        width: 100% !important;
        height: 800px !important;
        max-height: none !important;
    }
    
    .project-info {
        background: rgba(255,255,255,0.9);
        backdrop-filter: blur(10px);
        margin: 20px;
        padding: 30px;
        border-radius: 12px;
        box-shadow: 0 4px 16px rgba(0,0,0,0.1);
        max-width: 1200px;
        margin: 20px auto;
    }
    
    .project-info h3 {
        color: #2c5aa0;
        margin-top: 0;
        font-size: 20px;
    }
    
    .project-info p {
        line-height: 1.6;
        color: #555;
        margin-bottom: 15px;
    }
    
    .project-info strong {
        color: #2c5aa0;
    }
    
    .tableauPlaceholder {
        margin: 0 auto !important;
        display: block !important;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .dashboard-container {
            padding: 20px 10px;
            min-height: 70vh;
        }
        
        .project-info {
            margin: 10px;
            padding: 20px;
        }
    }
</style>

<div class="container">
    <div class="dashboard-container">
        <div class="dashboard-frame">
            <div class='tableauPlaceholder' id='viz1748947942078' style='position: relative'><noscript><a href='#'><img alt='Dashboard ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;fi&#47;final_dashboard_17487837319020&#47;Dashboard&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='final_dashboard_17487837319020&#47;Dashboard' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;fi&#47;final_dashboard_17487837319020&#47;Dashboard&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1748947942078');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='420px';vizElement.style.maxWidth='1200px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='none';vizElement.style.height= '1200px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='420px';vizElement.style.maxWidth='650px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='1000px';vizElement.style.height=(divElement.offsetWidth*1.00)+'px';} else { vizElement.style.width='100%';vizElement.style.height='2527px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
        </div>
    </div>

    <div class="project-info">
        <h3>🔬 Geological Knowledge Translation Dashboard</h3>
        <p><strong>Background:</strong> While working as a university assistant at Montanuniversität Leoben, I was assigned to develop classification algorithms for geological data. This experience revealed a fascinating problem that I wanted to explore further.</p>
        <p><strong>Personal Initiative:</strong> Using publicly available resources, I created this interactive dashboard to demonstrate why this isn't just a technical challenge - it's a science communication challenge about preserving expert knowledge.</p>
        <p><strong>Key Discovery:</strong> The same mineral assemblages can indicate different rock types depending on formation processes. Algorithms see lists of minerals, but geological experts read the story of how rocks formed - and that contextual knowledge gets lost in translation.</p>
        <p><strong>Real-World Impact:</strong> With 56 million tons of mineral waste generated annually in Austria, this knowledge translation gap has economic consequences - affecting recycling efficiency and circular economy goals.</p>
        <p><strong>Why This Matters:</strong> This project showcases my ability to identify complex problems, work with real data, and create engaging visualizations that make scientific concepts accessible to different audiences.</p>
    </div>
</div>
