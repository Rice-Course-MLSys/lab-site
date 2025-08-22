---
title: "Publications"
permalink: /publications/
layout: single
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.6"
  overlay_image: /assets/images/publications-banner.webp
  caption: "Photo credit: OpenAI-Sora"
excerpt: "Explore our latest research contributions published in top-tier conferences and journals."
---

<div class="publications-container">
  <!-- View Toggle Buttons -->
  <div class="view-toggle">
    <button id="year-view-btn" class="toggle-btn active">By Year</button>
    <button id="area-view-btn" class="toggle-btn">By Research Category</button>
  </div>

  <!-- Publications Content -->
  <div id="publications-content"></div>
</div>

<script>
// Centralized publications data - UPDATE ONLY HERE when adding new papers
const publicationsData = [
  {
    year: 2025,
    area: "Efficient",
    venue: "SOSP-2025",
    authors: "Yue Guan, Xinwei Qiang, Zaifeng Pan, Daniels Johnson, Yuanwei Fang, Keren Zhou, **Yuke Wang**, Wanlu Li, Yufei Ding, Adnan Aziz",
    title: "Mercury: Unlocking Multi-GPU Operator Optimization for LLMs via Remote Memory Scheduling",
    conference: "ACM Symposium on Operating Systems Principles",
    links: {
      paper: "https://storage.googleapis.com/yuke_profile/sosp25ae-paper4.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/2fd849fcbd6d4fe52faacb1c6f40ae0c5d6530d6/_publications/publication.bib#L192-L197",
      code: "https://github.com/ChandlerGuan/mercury_artifact"
    }
  },
  {
    year: 2025,
    area: "Scalable",
    venue: "SOSP-2025",
    authors: "Zhengding Hu, Vibha Murthy, Zaifeng Pan, Wanlu Li, Xiaoyi Fang, Yufei Ding, **Yuke Wang**",
    title: "HedraRAG: Coordinating LLM Generation and Database Retrieval in Heterogeneous RAG Serving",
    conference: "ACM Symposium on Operating Systems Principles",
    links: {
      paper: "https://arxiv.org/pdf/2507.09138",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/bda879dff0ec73d182b7dd38903ed752cd63b8c7/_publications/publication.bib#L185-L190",
      code: "https://github.com/Leo9660/HedraRAG_AE.git"
    }
  },
  {
    year: 2025,
    area: "Scalable",
    venue: "OSDI-2025",
    authors: "Zhuang Wang, Zhaozhuo Xu, Jingyi Xi, **Yuke Wang**, Anshumali Shrivastava, T. S. Eugene Ng",
    title: "Zen: Empowering Distributed Training with Sparsity-driven Data Synchronization",
    conference: "USENIX Symposium on Operating Systems Design and Implementation",
    links: {
      paper: "https://www.usenix.org/system/files/osdi25-wang-zhuang.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/af257edf7012b72f4409eedeba8b2d299df60e03/_publications/publication.bib#L171-L176",
      code: "https://github.com/zhuangwang93/ZEN",
      slides: "https://www.usenix.org/sites/default/files/conference/protected-files/osdi25_slides_wang_zhuang.pdf"
    }
  },
  {
    year: 2025,
    area: "Efficient",
    venue: "USENIX ATC-2025",
    authors: "**Yuke Wang**, Boyuan Feng, Zheng Wang, Guyue Huang, Tong Geng, Ang Li, Yufei Ding",
    title: "GMI-DRL: Empowering Multi-GPU DRL with Adaptive-Grained Parallelism",
    conference: "USENIX Annual Technical Conference",
    links: {
      paper: "https://www.usenix.org/system/files/atc25-wang-yuke.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/af257edf7012b72f4409eedeba8b2d299df60e03/_publications/publication.bib#L178-L183",
      code: "https://gitlab.com/YK-Wang96/gmi-drl-ae",
      slides: "https://storage.googleapis.com/yuke_profile/atc25-GMI-DRL_wang.pdf"
    }
  },
  {
    year: 2024,
    area: "Scalable",
    venue: "USENIX ATC-2024",
    authors: "Zheng Wang, **Yuke Wang**, Boyuan Feng, Guyue Huang, Dheevatsa Mudigere, Bharath Muthiah, Ang Li, Yufei Ding",
    title: "OPER: Optimality-Guided Embedding Table Parallelization for Large-scale Recommendation Model",
    conference: "USENIX Annual Technical Conference",
    links: {
      paper: "https://storage.googleapis.com/yuke_profile/ATC2024_OPER.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/68e4be5678b07ae405a286d842116e7c53c8051a/_publications/publication.bib#L164-L169"
    }
  },
  {
    year: 2024,
    area: "Efficient",
    venue: "ASPLOS-2024",
    authors: "Zheng Wang, **Yuke Wang**, Jiaqi Deng, Da Zheng, Ang Li, Yufei Ding",
    title: "RAP: Resource-aware Automated GPU Sharing for Multi-GPU Recommendation Model Training and Input Preprocessing",
    conference: "ACM International Conference on Architectural Support for Programming Languages and Operating Systems",
    links: {
      paper: "https://storage.googleapis.com/yuke_profile/ASPLOS24_RAP.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/56ed1be966fee4c0f452bd878d3f7837004eac96/_publications/publication.bib#L157-L162",
      code: "https://github.com/Ash-Zheng/RAP-artifacts"
    }
  },
  {
    year: 2024,
    area: "Secure",
    venue: "ASPLOS-2024",
    authors: "Boyuan Feng, Zheng Wang, **Yuke Wang**, Shu Yang, Yufei Ding",
    title: "ZENO: A Type-based Optimization Framework for Zero-Knowledge Neural Network Inference",
    conference: "ACM International Conference on Architectural Support for Programming Languages and Operating Systems",
    links: {
      paper: "https://storage.googleapis.com/yuke_profile/asplos24spring-final48.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/642f71bbf15e260224fabf5b22967c36b69ba932/_publications/publication.bib#L150-L155",
      code: "https://github.com/BoyuanFeng/ZENO"
    }
  },
  {
    year: 2023,
    area: "Efficient",
    venue: "OSDI-2023",
    authors: "**Yuke Wang**, Boyuan Feng, Zheng Wang, Tong Geng, Ang Li, Kevin Barker, Yufei Ding",
    title: "MGG: Accelerating Graph Neural Networks with Fine-grained intra-kernel Communication-Computation Pipelining on Multi-GPU Platforms",
    conference: "USENIX Symposium on Operating Systems Design and Implementation",
    links: {
      paper: "https://www.usenix.org/system/files/osdi23-wang-yuke.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/2ffc81e0832a8e7901d7d34c27c33868f9396f03/_publications/publication.bib#L143-L148",
      code: "https://github.com/YukeWang96/MGG-OSDI23-AE.git",
      slides: "https://storage.googleapis.com/yuke_profile/osdi23_slides_wang.pdf",
      video: "https://www.youtube.com/watch?v=HwykXVSa5hI"
    }
  },
  {
    year: 2023,
    area: "Efficient",
    venue: "USENIX ATC-2023",
    authors: "**Yuke Wang**, Boyuan Feng, Zheng Wang, Guyue Huang, Yufei Ding",
    title: "TC-GNN: Bridging Sparse GNN Computation and Dense Tensor Cores on GPUs",
    conference: "USENIX Annual Technical Conference",
    links: {
      paper: "https://www.usenix.org/system/files/atc23-wang-yuke.pdf",
      bibtex: "https://github.com/YukeWang96/personal_page/blob/1c3e27bb4a31ba2c40315179575fc3a21a1ef35d/_publications/publication.bib#L115-L120",
      code: "https://github.com/YukeWang96/TCGNN-Pytorch",
      slides: "https://storage.googleapis.com/yuke_profile/atc23_TC-GNN_wang_final.pdf",
      video: "https://www.youtube.com/watch?v=Et-kBEnry5Y"
    }
  },
  // Add more publications here following the same structure...
];

// Research areas mapping
const researchAreas = {
  "Efficient": [],
  "Scalable": [],
  "Secure": []
};

// Generate publication HTML
function generatePublicationHTML(pub) {
  const linksHTML = Object.entries(pub.links).map(([type, url]) => {
    const linkText = type.charAt(0).toUpperCase() + type.slice(1);
    return `<a href="${url}">[${linkText}]</a>`;
  }).join(' ');

  // Convert **text** to <strong>text</strong>
  const authorsHTML = pub.authors.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>');

  return `
    <div class="publication-item">
      <strong>[${pub.venue}]</strong> ${authorsHTML}<br>
      <em>${pub.title}</em><br>
      ${pub.conference}.<br>
      ${linksHTML}
    </div>
  `;
}

// Render publications by year
function renderByYear() {
  const yearGroups = {};
  publicationsData.forEach(pub => {
    if (!yearGroups[pub.year]) yearGroups[pub.year] = [];
    yearGroups[pub.year].push(pub);
  });

  const sortedYears = Object.keys(yearGroups).sort((a, b) => b - a);
  
  let html = '';
  sortedYears.forEach(year => {
    html += `<h2>${year}</h2>`;
    yearGroups[year].forEach(pub => {
      html += generatePublicationHTML(pub);
    });
  });

  document.getElementById('publications-content').innerHTML = html;
}

// Render publications by research area
function renderByArea() {
  const areaGroups = {};
  publicationsData.forEach(pub => {
    if (!areaGroups[pub.area]) areaGroups[pub.area] = [];
    areaGroups[pub.area].push(pub);
  });

  const sortedAreas = Object.keys(areaGroups).sort();
  
  let html = '';
  sortedAreas.forEach(area => {
    html += `<h2 id="${area.toLowerCase()}">${area}</h2>`;
    // Sort publications within each area by year (descending)
    areaGroups[area].sort((a, b) => b.year - a.year).forEach(pub => {
      html += generatePublicationHTML(pub);
    });
  });

  document.getElementById('publications-content').innerHTML = html;
}

// Toggle view functionality
document.addEventListener('DOMContentLoaded', function() {
  const yearBtn = document.getElementById('year-view-btn');
  const areaBtn = document.getElementById('area-view-btn');

  // Check if there's a hash in the URL indicating a specific category
  const hash = window.location.hash.substring(1); // Remove the # symbol
  const validCategories = ['efficient', 'scalable', 'secure'];
  
  if (hash && validCategories.includes(hash.toLowerCase())) {
    // Switch to area view and scroll to the specific category
    areaBtn.classList.add('active');
    yearBtn.classList.remove('active');
    renderByArea();
    
    // Scroll to the specific category after a brief delay to ensure rendering is complete
    setTimeout(() => {
      const categoryElement = document.getElementById(hash.toLowerCase());
      if (categoryElement) {
        categoryElement.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    }, 100);
  } else {
    // Default render by year
    renderByYear();
  }

  yearBtn.addEventListener('click', function() {
    yearBtn.classList.add('active');
    areaBtn.classList.remove('active');
    renderByYear();
    // Clear any hash from URL
    history.pushState('', document.title, window.location.pathname + window.location.search);
  });

  areaBtn.addEventListener('click', function() {
    areaBtn.classList.add('active');
    yearBtn.classList.remove('active');
    renderByArea();
  });
});
</script>

<style>
.publications-container {
  max-width: 100%;
  margin: 0 auto;
}

.view-toggle {
  display: flex;
  justify-content: center;
  margin-bottom: 2rem;
  gap: 1rem;
}

.toggle-btn {
  padding: 0.75rem 1.5rem;
  border: 2px solid #007acc;
  background-color: transparent;
  color: #007acc;
  cursor: pointer;
  border-radius: 5px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.toggle-btn:hover {
  background-color: #007acc;
  color: white;
}

.toggle-btn.active {
  background-color: #007acc;
  color: white;
}

.publication-item {
  margin-bottom: 1.5rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid #eee;
}

.publication-item:last-child {
  border-bottom: none;
}

.publication-item strong {
  color: #007acc;
}

.publication-item em {
  color: #333;
  font-style: italic;
}

.publication-item a {
  color: #007acc;
  text-decoration: none;
  margin-right: 0.5rem;
}

.publication-item a:hover {
  text-decoration: underline;
}

h2 {
  color: #2c3e50;
  border-bottom: 2px solid #007acc;
  padding-bottom: 0.5rem;
  margin-top: 2rem;
  margin-bottom: 1.5rem;
}

@media (max-width: 768px) {
  .view-toggle {
    flex-direction: column;
    align-items: center;
  }
  
  .toggle-btn {
    width: 200px;
  }
}
</style>

