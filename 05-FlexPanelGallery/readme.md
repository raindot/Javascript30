### 效果1. 打開一個panel時，已開過的不會收起來

    function toggleOpen(){
      this.classList.toggle('open');
    }

### 效果2. 打開一個panel時，已開過的會收起來

        function toggleOpen(){
          panels.forEach(panel => {
            if (panel.classList.contains('open')){
            panel.classList.remove('open');
            return;
            }
            if(this === panel){
              panel.classList.add('open');
            }
          });
        }