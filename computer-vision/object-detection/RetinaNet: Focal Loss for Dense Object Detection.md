# [RetinaNet: Focal Loss for Dense Object Detection](https://arxiv.org/pdf/1708.02002.pdf)

- The authors propose a novel loss they term the Focal Loss that adds a factor $(1 − p_t)^ γ$ to the standard cross entropy criterion. Setting γ > 0 reduces the relative loss for well-classified examples ($p_t$ > .5), putting more focus on hard, misclassified examples
